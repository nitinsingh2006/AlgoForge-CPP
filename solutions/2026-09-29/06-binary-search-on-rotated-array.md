# Binary Search on Rotated Array

**Difficulty:** Medium  
**Topic:** Search

Find target in rotated sorted array.

## Approach
Binary search with pivot detection.

## Complexity
O(log n) time, O(1) space

## Solution
```python
def solve(nums,target):
    l,r=0,len(nums)-1
    while l<=r:
        m=(l+r)//2
        if nums[m]==target:
            return m
        if nums[l]<=nums[m]:
            if nums[l]<=target<nums[m]:
                r=m-1
            else:
                l=m+1
        else:
            if nums[m]<target<=nums[r]:
                l=m+1
            else:
                r=m-1
    return -1
```

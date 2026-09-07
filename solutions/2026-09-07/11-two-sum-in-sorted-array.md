# Two Sum in Sorted Array

**Difficulty:** Easy  
**Topic:** Arrays

Given a sorted array of integers and a target sum, return the 1‑based indices of two numbers that add up to the target. If no such pair exists, return an empty list.

## Approach
Use two pointers: start at left and right ends, move inward based on sum comparison.

## Complexity
O(n) time, O(1) space

## Solution
```python
def two_sum_sorted(nums,target):
    l,r=0,len(nums)-1
    while l<r:
        s=nums[l]+nums[r]
        if s==target:
            return [l+1,r+1]
        elif s<target:
            l+=1
        else:
            r-=1
    return []
```

# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array nums and two indices left and right, reverse the elements between left and right inclusive. Return the modified array.

## Approach
Use two pointers moving towards each other, swapping elements until pointers cross.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,left,right):
    l,r=left,right
    while l<r:
        nums[l],nums[r]=nums[r],nums[l]
        l+=1
        r-=1
    return nums
```

# Reverse Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Given an array and indices L and R, reverse the subarray from L to R inclusive and return the modified array.

## Approach
Use two pointers moving inward, swapping elements until pointers cross.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,l,r):
    while l<r:
        nums[l],nums[r]=nums[r],nums[l]
        l+=1
        r-=1
    return nums
```

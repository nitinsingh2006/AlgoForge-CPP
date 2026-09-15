# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array nums and two indices l and r, reverse the elements from l to r inclusive in-place and return the modified array.

## Approach
Use two pointers starting at l and r, swapping elements until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums,l,r):\n    while l<r:\n        nums[l],nums[r]=nums[r],nums[l]\n        l+=1\n        r-=1\n    return nums
```

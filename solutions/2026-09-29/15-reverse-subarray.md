# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices L and R, reverse the elements between L and R inclusive.

## Approach
Use two pointers starting at L and R, swapping until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums, l, r):
    while l < r:
        nums[l], nums[r] = nums[r], nums[l]
        l += 1
        r -= 1
    return nums
```

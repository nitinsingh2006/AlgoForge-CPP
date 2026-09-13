# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices L and R, reverse the elements between L and R inclusive.

## Approach
Use two pointers starting at L and R, swapping elements until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(nums, l, r):\n    while l < r:\n        nums[l], nums[r] = nums[r], nums[l]\n        l += 1\n        r -= 1\n    return nums
```

# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the maximum sum of any contiguous subarray.

## Approach
Iterate once, keeping current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_sum = curr = nums[0]\n    for num in nums[1:]:\n        curr = max(num, curr+num)\n        max_sum = max(max_sum, curr)\n    return max_sum
```

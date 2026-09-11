# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Iterate through the array, keeping a running sum and updating the maximum when the running sum drops below zero.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_sum = curr = nums[0]
    for num in nums[1:]:
        curr = max(num, curr + num)
        max_sum = max(max_sum, curr)
    return max_sum
```

# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array nums, find the contiguous subarray with the largest sum and return that sum.

## Approach
Iterate through array, keep current sum and max sum, reset current sum to 0 if negative.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_sum = curr = nums[0]
    for num in nums[1:]:
        curr = max(num, curr + num)
        max_sum = max(max_sum, curr)
    return max_sum
```

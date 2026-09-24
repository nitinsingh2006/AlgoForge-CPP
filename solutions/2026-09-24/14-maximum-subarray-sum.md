# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Given an array of integers, find the contiguous subarray with the largest sum and return that sum. The subarray must contain at least one element.

## Approach
Kadane's algorithm: iterate, keep current sum and max sum.

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

# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an array of integers, return the maximum sum of a contiguous subarray.

## Approach
Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending = max_so_far = nums[0]
    for num in nums[1:]:
        max_ending = max(num, max_ending+num)
        max_so_far = max(max_so_far, max_ending)
    return max_so_far
```

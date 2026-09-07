# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm keeps current and max sums while scanning.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_so_far = curr = nums[0]
    for n in nums[1:]:
        curr = max(n, curr + n)
        max_so_far = max(max_so_far, curr)
    return max_so_far
```

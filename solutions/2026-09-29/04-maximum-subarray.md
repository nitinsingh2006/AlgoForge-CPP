# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm keeps current and global maximum while scanning.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending = max_so_far = nums[0]
    for num in nums[1:]:
        max_ending = max(num, max_ending + num)
        max_so_far = max(max_so_far, max_ending)
    return max_so_far
```

# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm tracks current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_ending = max_so_far = nums[0]\n    for n in nums[1:]:\n        max_ending = max(n, max_ending + n)\n        max_so_far = max(max_so_far, max_ending)\n    return max_so_far
```

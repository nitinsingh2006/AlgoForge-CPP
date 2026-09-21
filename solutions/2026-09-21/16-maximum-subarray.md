# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray within a one-dimensional array of numbers which has the largest sum. Return that sum.

## Approach
Use Kadane's algorithm: iterate through the array, keeping track of the maximum sum ending at the current position and the overall maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_ending = max_so_far = nums[0]\n    for num in nums[1:]:\n        max_ending = max(num, max_ending + num)\n        max_so_far = max(max_so_far, max_ending)\n    return max_so_far
```

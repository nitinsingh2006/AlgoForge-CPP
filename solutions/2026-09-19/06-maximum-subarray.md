# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm: keep current and global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):\n    max_ending = max_so_far = nums[0]\n    for num in nums[1:]:\n        max_ending = max(num, max_ending + num)\n        max_so_far = max(max_so_far, max_ending)\n    return max_so_far
```

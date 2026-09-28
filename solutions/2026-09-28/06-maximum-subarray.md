# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps a running maximum ending at each position.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve_max_subarray(nums):\n    max_ending = max_global = nums[0]\n    for num in nums[1:]:\n        max_ending = max(num, max_ending + num)\n        max_global = max(max_global, max_ending)\n    return max_global
```

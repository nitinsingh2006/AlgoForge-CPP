# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps current and global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_ending=max_global=nums[0]\n    for n in nums[1:]:\n        max_ending=max(n,max_ending+n)\n        max_global=max(max_global,max_ending)\n    return max_global
```

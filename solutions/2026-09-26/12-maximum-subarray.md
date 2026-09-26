# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps current and global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    best=curr=nums[0]\n    for n in nums[1:]:\n        curr=max(n, curr+n)\n        best=max(best, curr)\n    return best
```

# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm: iterate, keep current max and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    best=curr=nums[0]\n    for n in nums[1:]:\n        curr=max(n,curr+n)\n        best=max(best,curr)\n    return best
```

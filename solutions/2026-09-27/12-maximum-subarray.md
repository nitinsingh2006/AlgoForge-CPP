# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in a given integer array.

## Approach
Kadane's algorithm: iterate, keep current sum and max sum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_so_far=curr=nums[0]\n    for n in nums[1:]:\n        curr=max(n,curr+n)\n        max_so_far=max(max_so_far,curr)\n    return max_so_far
```

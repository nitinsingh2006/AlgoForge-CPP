# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in a given integer array.

## Approach
Kadane's algorithm tracks current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_ending=curr=nums[0]\n    for n in nums[1:]:\n        curr=max(n,curr+n)\n        max_ending=max(max_ending,curr)\n    return max_ending
```

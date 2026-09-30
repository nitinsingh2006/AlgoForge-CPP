# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Iterate through the array, keeping a running sum and resetting it to zero when it becomes negative. Track the maximum sum seen so far.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    max_sum=curr=nums[0]\n    for n in nums[1:]:\n        curr=max(n,curr+n)\n        max_sum=max(max_sum,curr)\n    return max_sum
```

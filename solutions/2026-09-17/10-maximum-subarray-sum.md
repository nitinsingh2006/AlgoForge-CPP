# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an array of integers, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm keeps a running sum and updates the maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):max_sum=curr=nums[0];i=1;while i<len(nums):curr=max(nums[i],curr+nums[i]);max_sum=max(max_sum,curr);i+=1;return max_sum
```

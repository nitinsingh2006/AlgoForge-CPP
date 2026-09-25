# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Iterate once, keeping current and best sums (Kadane's algorithm).

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): cur=best=nums[0]; for n in nums[1:]: cur=max(n,cur+n); best=max(best,cur); return best
```

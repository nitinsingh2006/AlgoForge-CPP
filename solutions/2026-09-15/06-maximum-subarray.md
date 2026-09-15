# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum. Return that maximum sum as an integer.

## Approach
Iterate through the array, keeping track of the current sum and maximum sum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): max_sum=curr=nums[0];
 for n in nums[1:]:
  curr=max(n, curr+n)
  max_sum=max(max_sum, curr)
 return max_sum
```

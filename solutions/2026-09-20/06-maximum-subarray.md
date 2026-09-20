# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum. Use Kadane's algorithm for an efficient solution.

## Approach
Apply Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): max_ending=max_so_far=nums[0];
 for n in nums[1:]:
  max_ending=max(n, max_ending+n);
  max_so_far=max(max_so_far, max_ending);
 return max_so_far
```

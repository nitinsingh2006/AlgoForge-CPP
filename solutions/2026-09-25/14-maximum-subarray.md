# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm: track current and maximum sums while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):max_so_far=curr=nums[0];[curr:=max(n,curr+n);max_so_far:=max(max_so_far,curr) for n in nums[1:]];return max_so_far
```

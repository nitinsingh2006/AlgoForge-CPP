# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array. Return that sum.

## Approach
Kadane's algorithm keeps current and global maximum while scanning once.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):max_so_far=curr=nums[0];[curr:=max(n,curr+n);max_so_far:=max(max_so_far,curr) for n in nums[1:]];return max_so_far
```

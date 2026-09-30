# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum and return that sum. The subarray must contain at least one element.

## Approach
Use Kadane's algorithm to keep track of current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_so_far=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        max_so_far=max(max_so_far,curr)
    return max_so_far
```

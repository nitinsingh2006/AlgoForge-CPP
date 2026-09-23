# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Kadane's algorithm keeps a running maximum ending at each position.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best=curr=nums[0]
    for n in nums[1:]:
        curr=max(n, curr+n)
        best=max(best, curr)
    return best
```

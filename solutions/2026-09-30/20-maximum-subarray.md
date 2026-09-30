# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Find the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_ending=curr=nums[0]
    for n in nums[1:]:
        curr=max(n, curr+n)
        max_ending=max(max_ending, curr)
    return max_ending
```

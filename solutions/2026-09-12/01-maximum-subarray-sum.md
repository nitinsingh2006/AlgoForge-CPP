# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, return the largest sum of any contiguous subarray.

## Approach
Iterate once, keeping current and best sums (Kadane's algorithm).

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best=cur=nums[0]
    for n in nums[1:]:
        cur=max(n,cur+n)
        best=max(best,cur)
    return best
```

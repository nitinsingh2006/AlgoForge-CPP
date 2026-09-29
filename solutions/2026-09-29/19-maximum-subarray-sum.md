# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, find the contiguous subarray with the largest sum and return that sum.

## Approach
Iterate once, keep current and best sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best = cur = nums[0]
    for x in nums[1:]:
        cur = x if cur < 0 else cur + x
        best = max(best, cur)
    return best
```

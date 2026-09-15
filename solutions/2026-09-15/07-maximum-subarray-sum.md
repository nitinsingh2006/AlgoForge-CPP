# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm tracks current and best sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best = cur = nums[0]
    for x in nums[1:]:
        cur = max(x, cur + x)
        best = max(best, cur)
    return best
```

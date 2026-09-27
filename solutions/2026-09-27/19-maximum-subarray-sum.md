# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the largest sum.

## Approach
Iterate, keep current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_ending_here = max_so_far = nums[0]
    for x in nums[1:]:
        max_ending_here = max(x, max_ending_here + x)
        max_so_far = max(max_so_far, max_ending_here)
    return max_so_far
```

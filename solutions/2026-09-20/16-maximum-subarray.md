# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the contiguous subarray with the maximum sum and return that sum. The subarray must contain at least one element.

## Approach
Iterate through the array, keeping a running maximum and updating the global best.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best=current=nums[0]
    for n in nums[1:]:
        current=max(n, current+n)
        best=max(best, current)
    return best
```

# Maximum Subarray Sum with One Deletion

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, find the maximum subarray sum where you may delete at most one element. Return the maximum sum achievable.

## Approach
Maintain two values: best ending here without deletion and best ending here with one deletion. Update iteratively using previous values.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubarraySumWithOneDeletion(nums):
    if not nums: return 0
    no_del = nums[0]
    one_del = 0
    best = nums[0]
    for x in nums[1:]:
        one_del = max(no_del, one_del + x)
        no_del = max(no_del + x, x)
        best = max(best, no_del, one_del)
    return best
```

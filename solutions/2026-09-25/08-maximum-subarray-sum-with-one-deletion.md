# Maximum Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Given an integer array nums, find the maximum sum of a subarray after deleting at most one element. Return the maximum sum.

## Approach
Maintain two DP values: keep (max sum ending here without deletion) and delete (max sum ending here with one deletion). Update iteratively.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_one_deletion(nums): keep = delete = nums[0]; best = nums[0]; for x in nums[1:]: keep = max(keep + x, x); delete = max(keep, delete + x); best = max(best, keep, delete); return best
```

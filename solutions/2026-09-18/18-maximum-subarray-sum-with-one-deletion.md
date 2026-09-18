# Maximum Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Given an integer array nums, find the maximum sum of a subarray after deleting at most one element. The subarray must contain at least one element.

## Approach
Maintain two DP values: max ending here without deletion and with one deletion. Update iteratively.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):
    if not nums:
        return 0
    no_del = nums[0]
    one_del = 0
    best = nums[0]
    for x in nums[1:]:
        one_del = max(no_del, one_del + x)
        no_del = max(no_del + x, x)
        best = max(best, no_del, one_del)
    return best
```

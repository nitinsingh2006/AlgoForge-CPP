# Maximum Subarray Sum with One Deletion

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, return the maximum sum of a subarray after deleting at most one element. The subarray must contain at least one element after deletion.

## Approach
Use two DP values: best without deletion and best with deletion. Update each step by extending or starting new subarray.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_one_del(nums):
    if not nums: return 0
    no_del = nums[0]
    with_del = 0
    best = nums[0]
    for x in nums[1:]:
        with_del = max(no_del, with_del + x)
        no_del = max(no_del + x, x)
        best = max(best, no_del, with_del)
    return best
```

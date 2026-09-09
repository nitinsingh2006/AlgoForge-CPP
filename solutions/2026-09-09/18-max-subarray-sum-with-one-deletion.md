# Max Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Given an integer array, find the maximum sum of a contiguous subarray where you may delete at most one element. Return that sum.

## Approach
Dynamic programming with two states: best ending here without deletion and with one deletion.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):\n    inc=dec=nums[0]\n    best=nums[0]\n    for x in nums[1:]:\n        prev_inc=inc\n        dec=max(prev_inc,dec+x)\n        inc=max(x,prev_inc+x)\n        best=max(best,inc,dec)\n    return best
```

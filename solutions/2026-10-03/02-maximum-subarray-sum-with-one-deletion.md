# Maximum Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Given an integer array nums, find the maximum sum of a contiguous subarray where you may delete at most one element. Return that sum.

## Approach
Maintain two DP arrays: one without deletion and one with one deletion, updating in O(1) per element.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_one_deletion(nums):
    if not nums:
        return 0
    no_del=del_one=nums[0]
    best=nums[0]
    for x in nums[1:]:
        del_one=max(no_del,x+del_one)
        no_del=max(no_del+x,x)
        best=max(best,no_del,del_one)
    return best
```

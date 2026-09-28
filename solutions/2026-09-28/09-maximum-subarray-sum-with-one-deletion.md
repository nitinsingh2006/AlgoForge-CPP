# Maximum Subarray Sum with One Deletion

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array, return the maximum sum of a subarray after deleting at most one element.

## Approach
Use two DP states: max ending here without deletion and with one deletion. Update iteratively.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_one_deletion(nums):
    n=len(nums)
    if n==1:
        return nums[0]
    no_del=nums[0]
    one_del=0
    best=no_del
    for i in range(1,n):
        one_del=max(no_del, one_del+nums[i])
        no_del=max(no_del+nums[i], nums[i])
        best=max(best, no_del, one_del)
    return best
```

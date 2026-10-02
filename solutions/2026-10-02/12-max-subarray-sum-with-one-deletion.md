# Max Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Dynamic Programming

Find the maximum sum of a contiguous subarray after deleting at most one element from the array.

## Approach
Maintain two DP states: best sum ending here without deletion and with one deletion.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_one_del(nums):
    n=len(nums)
    if n==0:return 0
    no_del=nums[0]
    one_del=0
    best=nums[0]
    for i in range(1,n):
        one_del=max(no_del,one_del+nums[i])
        no_del=max(nums[i],no_del+nums[i])
        best=max(best,no_del,one_del)
    return best
```

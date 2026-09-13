# Max Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Dynamic Programming

Given an integer array nums, return the maximum sum of a non‑empty subarray after deleting at most one element.

## Approach
Maintain two DP values: keep (max sum ending at i without deletion) and delete (max sum ending at i with one deletion). Update iteratively.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):
    keep=delete=nums[0]
    ans=nums[0]
    for x in nums[1:]:
        delete=max(delete+x,keep)
        keep=max(keep+x,x)
        ans=max(ans,keep,delete)
    return ans
```

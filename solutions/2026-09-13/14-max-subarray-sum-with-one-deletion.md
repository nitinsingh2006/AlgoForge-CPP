# Max Subarray Sum with One Deletion

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an integer array nums, find the maximum sum of a non‑empty subarray after deleting at most one element.

## Approach
Maintain two DP arrays: keep[i] max sum ending at i without deletion, del[i] with one deletion. Update in O(n).

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):\n    keep=del_=nums[0]\n    ans=nums[0]\n    for x in nums[1:]:\n        del_=max(keep,del_+x)\n        keep=max(keep+x,x)\n        ans=max(ans,keep,del_)\n    return ans
```

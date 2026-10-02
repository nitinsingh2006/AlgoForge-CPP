# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array, return the sum of the contiguous subarray with the largest sum.

## Approach
Kadane's algorithm scans once, keeping current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    cur=best=nums[0]
    for x in nums[1:]:
        cur=max(x,cur+x)
        best=max(best,cur)
    return best
```

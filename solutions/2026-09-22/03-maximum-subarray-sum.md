# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Given an integer array, return the largest sum of any contiguous subarray.

## Approach
Kadane's algorithm: keep current and global max.

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

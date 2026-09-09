# Maximum Subarray

**Difficulty:** Medium  
**Topic:** DP

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    cur=best=nums[0]
    for n in nums[1:]:
        cur=max(n,cur+n)
        best=max(best,cur)
    return best
```

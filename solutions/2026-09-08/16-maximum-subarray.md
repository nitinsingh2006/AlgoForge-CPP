# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in a given integer array.

## Approach
Kadane's algorithm: track current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):\n    cur=best=nums[0]\n    for n in nums[1:]:\n        cur=max(n,cur+n)\n        best=max(best,cur)\n    return best
```

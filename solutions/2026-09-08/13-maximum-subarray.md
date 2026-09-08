# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the maximum sum in an integer array.

## Approach
Iterate once, keeping current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums):\n    cur=best=nums[0]\n    for x in nums[1:]:\n        cur=max(x,cur+x)\n        best=max(best,cur)\n    return best
```

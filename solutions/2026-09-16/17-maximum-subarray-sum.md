# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Find the maximum sum of any contiguous subarray in a given integer array.

## Approach
Use Kadane's algorithm to track current and global maximum.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums): cur=0; best=nums[0];\n    for x in nums:\n        cur=max(x,cur+x); best=max(best,cur)\n    return best
```

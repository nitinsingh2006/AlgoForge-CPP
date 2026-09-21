# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm keeps current and global maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    cur=best=nums[0]
    for n in nums[1:]:
        cur=max(n,cur+n)
        best=max(best,cur)
    return best
```

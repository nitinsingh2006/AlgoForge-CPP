# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Return max sum of contiguous subarray.

## Approach
Kadane's algorithm: track current and max sums.

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

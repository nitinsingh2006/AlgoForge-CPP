# Max Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Find the maximum sum of a subarray after deleting at most one element from the array.

## Approach
Maintain two DP states: keep and delete. Update iteratively.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_one_deletion(nums):\n    keep=delete=nums[0]\n    best=nums[0]\n    for x in nums[1:]:\n        delete=keep+x\n        keep=max(x,keep+x)\n        best=max(best,keep,delete)\n    return best
```

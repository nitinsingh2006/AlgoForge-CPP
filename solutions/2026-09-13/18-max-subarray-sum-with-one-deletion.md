# Max Subarray Sum with One Deletion

**Difficulty:** Hard  
**Topic:** Arrays

Find the maximum subarray sum after deleting at most one element from the array.

## Approach
Maintain two DP arrays: keep[i] for max sum ending at i without deletion, del[i] for max sum ending at i with one deletion.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray_sum_with_deletion(nums):\n    if not nums:\n        return 0\n    keep = del_ = nums[0]\n    best = nums[0]\n    for x in nums[1:]:\n        del_ = max(keep, del_ + x)\n        keep = max(keep + x, x)\n        best = max(best, keep, del_)\n    return best
```

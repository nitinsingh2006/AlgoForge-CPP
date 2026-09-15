# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Arrays

Find the maximum sum of a contiguous subarray in a given integer array.

## Approach
Kadane's algorithm: track current and global max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_so_far = nums[0]
    curr_max = nums[0]
    for num in nums[1:]:
        curr_max = max(num, curr_max + num)
        max_so_far = max(max_so_far, curr_max)
    return max_so_far
```

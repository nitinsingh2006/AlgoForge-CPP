# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Find the contiguous subarray within an array that has the largest sum.

## Approach
Apply Kadane's algorithm to track current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_so_far = curr = nums[0]
    for num in nums[1:]:
        curr = max(num, curr + num)
        max_so_far = max(max_so_far, curr)
    return max_so_far
```

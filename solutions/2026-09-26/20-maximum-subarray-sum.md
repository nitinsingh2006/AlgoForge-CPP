# Maximum Subarray Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray within an array that has the largest sum.

## Approach
Use Kadane's algorithm, tracking current and maximum sums while iterating.

## Complexity
O(n) time, O(1) space

## Solution
```python
def maxSubArray(nums):
    max_so_far = curr = nums[0]
    for num in nums[1:]:
        curr = max(num, curr + num)
        max_so_far = max(max_so_far, curr)
    return max_so_far
```

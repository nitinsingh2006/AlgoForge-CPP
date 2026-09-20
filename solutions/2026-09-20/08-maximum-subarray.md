# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Find the contiguous subarray within an array of integers that has the largest sum.

## Approach
Apply Kadane's algorithm, tracking current and maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_so_far=nums[0]
    current=nums[0]
    for num in nums[1:]:
        current=max(num,current+num)
        max_so_far=max(max_so_far,current)
    return max_so_far
```

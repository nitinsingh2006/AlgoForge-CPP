# Maximum Subarray

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the maximum sum in a given integer array.

## Approach
Apply Kadane's algorithm to track current and global maximum sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_ending=max_so_far=nums[0]
    for num in nums[1:]:
        max_ending=max(num,max_ending+num)
        max_so_far=max(max_so_far,max_ending)
    return max_so_far
```

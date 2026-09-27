# Maximum Subarray Sum

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Find the contiguous subarray with the largest sum in an integer array.

## Approach
Kadane's algorithm tracks current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):max_ending=0;max_so_far=float('-inf');for x in nums:max_ending=max(x,max_ending+x);max_so_far=max(max_so_far,max_ending);return max_so_far
```

# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Find the contiguous subarray within a one-dimensional array of numbers which has the largest sum and return that sum.

## Approach
Use Kadane's algorithm: iterate, keeping current sum and max sum, resetting current sum to 0 when it becomes negative.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_so_far=nums[0]
    cur=nums[0]
    for n in nums[1:]:
        cur=max(n,cur+n)
        max_so_far=max(max_so_far,cur)
    return max_so_far
```

# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Find the contiguous subarray within an array that has the largest sum.

## Approach
Use Kadane's algorithm: iterate through the array, maintaining current sum and maximum sum seen so far. Update current sum by taking the maximum of the current element and current sum plus the element. Update maximum sum accordingly.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_so_far=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        max_so_far=max(max_so_far,curr)
    return max_so_far
```

# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Return the largest sum of any contiguous subarray.

## Approach
Kadane's algorithm maintains current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    max_ending=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        max_ending=max(max_ending,curr)
    return max_ending
```

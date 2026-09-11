# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Dynamic Programming

Return the largest sum of a contiguous subarray.

## Approach
Kadane's algorithm keeps a running max.

## Complexity
O(n) time, O(1) space

## Solution
```python
def max_subarray(nums):
    best=curr=nums[0]
    for n in nums[1:]:
        curr=max(n,curr+n)
        best=max(best,curr)
    return best
```

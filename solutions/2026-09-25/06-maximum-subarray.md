# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Return the largest sum of a contiguous subarray.

## Approach
Kadane's algorithm tracks current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_so_far=nums[0]
    max_ending=nums[0]
    for x in nums[1:]:
        max_ending=max(x,max_ending+x)
        max_so_far=max(max_so_far,max_ending)
    return max_so_far
```

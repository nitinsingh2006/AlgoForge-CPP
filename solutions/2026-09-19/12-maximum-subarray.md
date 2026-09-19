# Maximum Subarray

**Difficulty:** Easy  
**Topic:** Arrays

Return the largest sum of a contiguous subarray.

## Approach
Kadane's algorithm: track current and max sums.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(nums):
    max_sum = curr = nums[0]
    for num in nums[1:]:
        curr = max(num, curr + num)
        max_sum = max(max_sum, curr)
    return max_sum
```

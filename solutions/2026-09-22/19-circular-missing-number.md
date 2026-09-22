# Circular Missing Number

**Difficulty:** Medium  
**Topic:** Arrays

You are given a circular array of length n containing integers from 1 to n, but one number is missing and another appears twice. Find the missing number.

## Approach
Compute expected sum and sum of squares, then solve for missing and duplicate.

## Complexity
O(n) time, O(1) space

## Solution
```python
def find_missing(nums):\n    n = len(nums)\n    sum_expected = n*(n+1)//2\n    sum_actual = sum(nums)\n    sum_sq_expected = n*(n+1)*(2*n+1)//6\n    sum_sq_actual = sum(x*x for x in nums)\n    diff = sum_expected - sum_actual\n    sum_sq_diff = sum_sq_expected - sum_sq_actual\n    xy = sum_sq_diff // diff\n    missing = (xy + diff) // 2\n    return missing
```

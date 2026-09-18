# Find Missing Number

**Difficulty:** Easy  
**Topic:** Arrays

Given n-1 distinct numbers from 1 to n, find the missing number.

## Approach
Compute the expected sum 1+2+...+n and subtract the actual sum of the array.

## Complexity
O(n) time, O(1) space

## Solution
```python
def missing(nums): n=len(nums)+1; return n*(n+1)//2 - sum(nums)
```

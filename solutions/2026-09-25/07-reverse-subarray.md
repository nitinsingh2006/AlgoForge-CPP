# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array arr and indices L and R, reverse the subarray arr[L:R+1] in place and return the modified array.

## Approach
Swap elements from both ends moving towards center.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(arr, L, R): while L < R: arr[L], arr[R] = arr[R], arr[L]; L += 1; R -= 1; return arr
```

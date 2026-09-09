# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices L and R, reverse the subarray from L to R inclusive. Return the modified array.

## Approach
Use two pointers to swap elements until the middle.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(arr,l,r):\n    while l<r:\n        arr[l],arr[r]=arr[r],arr[l]\n        l+=1\n        r-=1\n    return arr
```

# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an integer array and two indices L and R, reverse the elements between L and R inclusive in place. Return the modified array.

## Approach
Use two pointers to swap elements from both ends until they meet.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_subarray(arr,l,r):
    while l<r:
        arr[l],arr[r]=arr[r],arr[l]
        l+=1
        r-=1
    return arr
```

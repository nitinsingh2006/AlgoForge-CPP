# Reverse Subarray

**Difficulty:** Medium  
**Topic:** Arrays

Given an array and two indices L and R, reverse the subarray from L to R inclusive. Return the modified array.

## Approach
Use two pointers to swap elements until the pointers meet.

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

# Binary Search on Sorted Array

**Difficulty:** Medium  
**Topic:** Search

Return index of target in sorted array or -1 if not found.

## Approach
Iterative binary search.

## Complexity
O(log n) time, O(1) space

## Solution
```python
def solve(arr,target):
    l,r=0,len(arr)-1
    while l<=r:
        m=(l+r)//2
        if arr[m]==target:
            return m
        elif arr[m]<target:
            l=m+1
        else:
            r=m-1
    return -1
```

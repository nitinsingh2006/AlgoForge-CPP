# Minimum Swaps to Sort

**Difficulty:** Medium  
**Topic:** Sorting

Given an array of distinct integers, find the minimum number of swaps required to sort it in ascending order.

## Approach
Use cycle detection on the permutation of indices to compute swaps.

## Complexity
O(n log n) time, O(n) space

## Solution
```python
def solve(arr):
    n=len(arr)
    arr_pos=sorted(enumerate(arr), key=lambda it: it[1])
    visited=[False]*n
    swaps=0
    for i in range(n):
        if visited[i] or arr_pos[i][0]==i:
            continue
        cycle_size=0
        j=i
        while not visited[j]:
            visited[j]=True
            j=arr_pos[j][0]
            cycle_size+=1
        if cycle_size>0:
            swaps+=cycle_size-1
    return swaps
```

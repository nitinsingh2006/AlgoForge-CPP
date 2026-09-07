# Minimum Swaps to Sort an Array

**Difficulty:** Medium  
**Topic:** Graph

Given an array of distinct integers, determine the minimum number of swaps required to sort the array in ascending order.

## Approach
Treat the array as a permutation and count cycles; each cycle of length L requires L-1 swaps.

## Complexity
O(n log n) time for sorting + O(n) for cycle detection, O(n) space

## Solution
```python
def solve(arr):
    n=len(arr)
    visited=[False]*n
    sorted_arr=sorted((val,i) for i,val in enumerate(arr))
    pos=[0]*n
    for sorted_idx,(val,orig_idx) in enumerate(sorted_arr):
        pos[orig_idx]=sorted_idx
    swaps=0
    for i in range(n):
        if visited[i] or pos[i]==i:
            continue
        cycle=0
        j=i
        while not visited[j]:
            visited[j]=True
            j=pos[j]
            cycle+=1
        swaps+=cycle-1
    return swaps
```

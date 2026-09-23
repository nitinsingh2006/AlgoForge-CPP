# Minimum Swaps to Group Ones

**Difficulty:** Hard  
**Topic:** Arrays

Given a binary array, find the minimum number of adjacent swaps required to group all 1s together. Swaps can only be performed between neighboring elements.

## Approach
Use a sliding window of size equal to the total number of 1s. Count zeros inside the window; the minimum zeros encountered equals the answer.

## Complexity
O(n) time, O(1) space

## Solution
```python
def min_swaps(arr):\n    ones=sum(arr)\n    if ones<=1: return 0\n    zeros=sum(1 for i in range(ones) if arr[i]==0)\n    min_zeros=zeros\n    for i in range(ones,len(arr)):\n        if arr[i-ones]==0: zeros+=1\n        if arr[i]==0: zeros-=1\n        if zeros<min_zeros: min_zeros=zeros\n    return min_zeros
```

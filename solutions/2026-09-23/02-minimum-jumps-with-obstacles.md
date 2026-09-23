# Minimum Jumps with Obstacles

**Difficulty:** Hard  
**Topic:** Arrays

Given an array arr where arr[i] denotes the maximum jump length from index i, and an array blocked of same length where blocked[i] is true if index i is blocked, find the minimum number of jumps to reach the last index. Return -1 if impossible.

## Approach
Greedy scan updating farthest reachable index while skipping blocked positions.

## Complexity
O(n) time, O(1) space

## Solution
```python
def minJumps(arr, blocked):\n    n=len(arr)\n    if n==0 or blocked[0]:\n        return -1\n    if n==1:\n        return 0\n    jumps=0\n    current_end=0\n    farthest=0\n    for i in range(n-1):\n        if blocked[i]:\n            continue\n        farthest=max(farthest, i+arr[i])\n        if i==current_end:\n            jumps+=1\n            current_end=farthest\n            if current_end>=n-1:\n                return jumps\n    return -1
```

# Longest Increasing Path in a Matrix

**Difficulty:** Hard  
**Topic:** DP

Given a matrix of integers, find the length of the longest strictly increasing path. You can move up, down, left, or right.

## Approach
DFS with memoization to cache longest path from each cell.

## Complexity
O(m*n) time, O(m*n) space

## Solution
```python
def longestIncreasingPath(matrix):\n    if not matrix: return 0\n    m, n = len(matrix), len(matrix[0])\n    from functools import lru_cache\n    dirs = [(1,0),(-1,0),(0,1),(0,-1)]\n    @lru_cache(None)\n    def dfs(i,j):\n        best = 1\n        for di,dj in dirs:\n            ni, nj = i+di, j+dj\n            if 0<=ni<m and 0<=nj<n and matrix[ni][nj] > matrix[i][j]:\n                best = max(best, 1+dfs(ni,nj))\n        return best\n    return max(dfs(i,j) for i in range(m) for j in range(n))
```

# Unique Paths with Obstacles

**Difficulty:** Medium  
**Topic:** Dynamic Programming

Given an m x n grid where 1 represents an obstacle and 0 a free cell, count the number of unique paths from top-left to bottom-right moving only right or down.

## Approach
Dynamic programming: dp[i][j] = dp[i-1][j] + dp[i][j-1] if cell free.

## Complexity
O(mn) time, O(mn) space

## Solution
```python
def solve(grid):
    if not grid or not grid[0]:
        return 0
    m, n = len(grid), len(grid[0])
    dp = [[0]*n for _ in range(m)]
    for i in range(m):
        for j in range(n):
            if grid[i][j] == 1:
                dp[i][j] = 0
            elif i == 0 and j == 0:
                dp[i][j] = 1
            else:
                dp[i][j] = (dp[i-1][j] if i>0 else 0) + (dp[i][j-1] if j>0 else 0)
    return dp[m-1][n-1]
```

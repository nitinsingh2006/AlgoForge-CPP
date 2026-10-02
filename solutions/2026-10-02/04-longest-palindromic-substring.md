# Longest Palindromic Substring

**Difficulty:** Medium  
**Topic:** Strings

Return the longest palindromic substring in a given string.

## Approach
Expand around centers for each character pair.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def solve(s):\n    if not s:return ''\n    start=0;end=0\n    for i in range(len(s)):\n        for l,r in ((i,i),(i,i+1)):\n            while l>=0 and r<len(s) and s[l]==s[r]:\n                l-=1;r+=1\n            if r-l-1>end-start:\n                start=l+1;end=r-1\n    return s[start:end+1]
```

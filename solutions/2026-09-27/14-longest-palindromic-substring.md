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
def solve(s):
    if not s:return ''
    start=0;end=0
    for i in range(len(s)):
        for l,r in ((i,i),(i,i+1)):
            while l>=0 and r<len(s) and s[l]==s[r]:
                l-=1;r+=1
            if r-l-1>end-start:
                start=l+1;end=r-1
    return s[start:end+1]
```

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
    start=0
    end=0
    for i in range(len(s)):
        for left,right in ((i,i),(i,i+1)):
            while left>=0 and right<len(s) and s[left]==s[right]:
                left-=1
                right+=1
            if right-left-1> end-start:
                start=left+1
                end=right
    return s[start:end]
```

# Longest Palindromic Substring

**Difficulty:** Hard  
**Topic:** Strings

Given a string, return the longest contiguous substring that is a palindrome.

## Approach
Expand around each center to find palindromes.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def longest_palindrome(s):
    if not s:return""
    start=0
    end=0
    for i in range(len(s)):
        l=r=i
        while l>=0 and r<len(s) and s[l]==s[r]:
            l-=1
            r+=1
        if r-l-1>end-start:
            start=l+1
            end=r-1
        l=r=i
        r+=1
        while l>=0 and r<len(s) and s[l]==s[r]:
            l-=1
            r+=1
        if r-l-1>end-start:
            start=l+1
            end=r-1
    return s[start:end+1]
```

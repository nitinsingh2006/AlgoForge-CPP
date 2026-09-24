# Longest Palindromic Substring

**Difficulty:** Hard  
**Topic:** Strings

Find the longest substring of a given string that reads the same forwards and backwards.

## Approach
Expand around each center (odd and even length) to find palindromes and keep the longest.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def expand(s,left,right):
    while left>=0 and right<len(s) and s[left]==s[right]:
        left-=1
        right+=1
    return right-left-1

def longest_palindrome(s):
    if not s:
        return ''
    start=end=0
    for i in range(len(s)):
        l1=expand(s,i,i)
        l2=expand(s,i,i+1)
        l=max(l1,l2)
        if l>end-start:
            start=i-(l-1)//2
            end=i+l//2
    return s[start:end+1]
```

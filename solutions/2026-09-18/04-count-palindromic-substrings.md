# Count Palindromic Substrings

**Difficulty:** Hard  
**Topic:** Strings

Count all palindromic substrings in a given string.

## Approach
Expand around each center to find palindromes.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def count_palindromes(s):\n    n=len(s)\n    cnt=0\n    for c in range(2*n-1):\n        l=c//2\n        r=l+c%2\n        while l>=0 and r<n and s[l]==s[r]:\n            cnt+=1\n            l-=1\n            r+=1\n    return cnt
```

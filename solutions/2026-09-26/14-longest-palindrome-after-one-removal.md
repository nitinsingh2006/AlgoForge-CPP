# Longest Palindrome After One Removal

**Difficulty:** Hard  
**Topic:** Strings

Given a string s, find the length of the longest substring that can become a palindrome by removing at most one character.

## Approach
Expand around each center allowing at most one mismatch to account for the removal.

## Complexity
O(n^2) time, O(1) space

## Solution
```python
def longest_palindrome_one_removal(s):
    n = len(s)
    best = 0
    for center in range(n):
        l = r = center
        mism = 0
        while l >= 0 and r < n:
            if s[l] != s[r]:
                mism += 1
                if mism > 1:
                    break
            l -= 1
            r += 1
        best = max(best, r - l - 1)
        l, r = center, center + 1
        mism = 0
        while l >= 0 and r < n:
            if s[l] != s[r]:
                mism += 1
                if mism > 1:
                    break
            l -= 1
            r += 1
        best = max(best, r - l - 1)
    return best
```

# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find the length of the longest substring in a string that contains no repeated characters.

## Approach
Sliding window with a set to track current characters.

## Complexity
O(n) time, O(min(n, alphabet)) space

## Solution
```python
def solve(s):
    seen = {}
    left = 0
    max_len = 0
    for right, ch in enumerate(s):
        if ch in seen and seen[ch] >= left:
            left = seen[ch] + 1
        seen[ch] = right
        max_len = max(max_len, right - left + 1)
    return max_len
```

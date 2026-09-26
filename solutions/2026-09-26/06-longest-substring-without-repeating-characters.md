# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find the length of the longest substring without duplicate characters in a given string.

## Approach
Sliding window with a set to track current characters.

## Complexity
O(n) time, O(min(n, alphabet)) space

## Solution
```python
def longest_substring(s):\n    seen = set()\n    left = 0\n    max_len = 0\n    for right, char in enumerate(s):\n        while char in seen:\n            seen.remove(s[left])\n            left += 1\n        seen.add(char)\n        max_len = max(max_len, right - left + 1)\n    return max_len
```

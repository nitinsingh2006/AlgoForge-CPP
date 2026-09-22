# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find length of longest substring without duplicate characters in a given string.

## Approach
Sliding window with a set to track characters.

## Complexity
O(n) time, O(min(n, m)) space

## Solution
```python
def length_of_longest_substring(s):\n    seen={}\n    left=0\n    max_len=0\n    for right,ch in enumerate(s):\n        if ch in seen and seen[ch]>=left:\n            left=seen[ch]+1\n        seen[ch]=right\n        max_len=max(max_len,right-left+1)\n    return max_len
```

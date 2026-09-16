# Longest Substring Without Repeating Characters

**Difficulty:** Medium  
**Topic:** Strings

Find the length of the longest substring without repeating characters in a given string.

## Approach
Sliding window with a set to track characters.

## Complexity
O(n) time, O(min(n, alphabet)) space

## Solution
```python
def length_of_longest_substring(s):
    seen={}
    left=0
    maxlen=0
    for right,ch in enumerate(s):
        if ch in seen and seen[ch]>=left:
            left=seen[ch]+1
        seen[ch]=right
        maxlen=max(maxlen,right-left+1)
    return maxlen
```

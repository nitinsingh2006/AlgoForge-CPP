# Balanced Parentheses

**Difficulty:** Medium  
**Topic:** Strings

Check if a string of parentheses is balanced using a stack.

## Approach
Iterate characters, push opening, pop on closing, ensure matches.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(s):
    stack=[]
    mapping={')':'(',']':'[','}':'{'}
    for ch in s:
        if ch in mapping.values():
            stack.append(ch)
        elif ch in mapping:
            if not stack or stack[-1]!=mapping[ch]:
                return False
            stack.pop()
    return not stack
```

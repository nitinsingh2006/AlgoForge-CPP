# Balanced Parentheses

**Difficulty:** Medium  
**Topic:** Strings

Check if a string of parentheses is balanced.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def solve(s):
    stack=[]
    mapping={')':'(',']':'[','}':'{'}
    for c in s:
        if c in mapping.values():
            stack.append(c)
        elif c in mapping:
            if not stack or stack[-1]!=mapping[c]:
                return False
            stack.pop()
    return not stack
```

# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Determine if a string of parentheses is balanced.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s):
    stack=[]
    mapping={')':'(', ']':'[', '}':'{'}
    for ch in s:
        if ch in mapping.values():
            stack.append(ch)
        elif ch in mapping:
            if not stack or stack[-1]!=mapping[ch]:
                return False
            stack.pop()
    return not stack
```

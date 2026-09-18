# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Given a string s containing only '(', ')', '{', '}', '[' and ']', determine if the brackets are properly closed and nested.

## Approach
Use a stack to match opening and closing brackets.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s):\n    stack=[]\n    mapping={')':'(', '}':'{', ']':'['}\n    for ch in s:\n        if ch in mapping.values():\n            stack.append(ch)\n        elif ch in mapping:\n            if not stack or stack[-1]!=mapping[ch]:\n                return False\n            stack.pop()\n    return not stack
```

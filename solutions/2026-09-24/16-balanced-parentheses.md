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
def solve(s):\n    stack=[]\n    mapping={')':'(',']':'[','}':'{'}\n    for c in s:\n        if c in mapping.values():\n            stack.append(c)\n        elif c in mapping:\n            if not stack or stack[-1]!=mapping[c]:\n                return False\n            stack.pop()\n    return not stack
```

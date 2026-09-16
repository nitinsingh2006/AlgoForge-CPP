# Balanced Parentheses

**Difficulty:** Easy  
**Topic:** Strings

Given a string of parentheses '(', ')', determine if it is properly balanced.

## Approach
Use a stack to match opening and closing.

## Complexity
O(n) time, O(n) space

## Solution
```python
def is_balanced(s): stack=[]; for c in s: if c=='(': stack.append(c); elif c==')': if not stack: return False; stack.pop(); return not stack
```

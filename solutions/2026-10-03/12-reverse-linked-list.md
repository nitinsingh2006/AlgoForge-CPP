# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked Lists

Reverse a singly linked list and return its head.

## Approach
Iteratively rewire next pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
def solve(head):\n    prev=None\n    curr=head\n    while curr:\n        nxt=curr.next\n        curr.next=prev\n        prev=curr\n        curr=nxt\n    return prev
```

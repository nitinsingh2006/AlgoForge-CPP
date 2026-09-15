# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Given the head of a singly linked list, reverse the list and return the new head.

## Approach
Iteratively reverse pointers using three pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverseList(head):\n    prev=None\n    curr=head\n    while curr:\n        nxt=curr.next\n        curr.next=prev\n        prev=curr\n        curr=nxt\n    return prev
```

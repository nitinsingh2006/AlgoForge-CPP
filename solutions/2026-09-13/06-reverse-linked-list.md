# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Reverse a singly linked list and return its head.

## Approach
Iteratively reverse pointers using three references.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverseList(head):
    prev=None
    curr=head
    while curr:
        nxt=curr.next
        curr.next=prev
        prev=curr
        curr=nxt
    return prev
```

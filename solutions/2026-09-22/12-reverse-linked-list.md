# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked Lists

Reverse a singly linked list in place.

## Approach
Iteratively reverse pointers using three variables.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_list(head):prev=None;curr=head;while curr:nxt=curr.next;curr.next=prev;prev=curr;curr=nxt;return prev
```

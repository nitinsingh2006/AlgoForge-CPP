# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Reverse a singly linked list and return its head.

## Approach
Iteratively rewire next pointers using three pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverseList(head):prev=None;curr=head;while curr:next=curr.next;curr.next=prev;prev=curr;curr=next;return prev
```

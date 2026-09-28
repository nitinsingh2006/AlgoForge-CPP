# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Given the head of a singly linked list, reverse the list and return the new head.

## Approach
Iteratively reverse pointers using three variables.

## Complexity
O(n) time, O(1) space

## Solution
```python
def reverse_list(head):prev=None;curr=head;while curr:next=curr.next;curr.next=prev;prev=curr;curr=next;return prev
```

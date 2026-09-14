# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked Lists

Given head of a singly linked list, reverse it and return new head.

## Approach
Iteratively change next pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:
    def __init__(self,val=0,next=None):
        self.val=val
        self.next=next

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

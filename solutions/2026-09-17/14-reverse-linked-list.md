# Reverse Linked List

**Difficulty:** Medium  
**Topic:** Linked List

Reverse a singly linked list and return its head.

## Approach
Iteratively rewire next pointers.

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

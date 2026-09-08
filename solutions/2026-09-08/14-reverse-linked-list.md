# Reverse Linked List

**Difficulty:** Easy  
**Topic:** Linked Lists

Reverse a singly linked list and return its head.

## Approach
Iteratively rewire next pointers.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:\n    def __init__(self,val=0,next=None):\n        self.val=val\n        self.next=next\n\ndef reverseList(head):\n    prev=None\n    cur=head\n    while cur:\n        nxt=cur.next\n        cur.next=prev\n        prev=cur\n        cur=nxt\n    return prev
```

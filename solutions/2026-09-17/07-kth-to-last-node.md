# Kth to Last Node

**Difficulty:** Medium  
**Topic:** Linked List

Return the value of the kth node from the end of a singly linked list.

## Approach
Use two pointers separated by k nodes.

## Complexity
O(n) time, O(1) space

## Solution
```python
class ListNode:
    def __init__(self,val=0,next=None):
        self.val=val
        self.next=next

def kth_to_last(head,k):
    fast=head
    for _ in range(k):
        if not fast: return None
        fast=fast.next
    slow=head
    while fast:
        fast=fast.next
        slow=slow.next
    return slow.val
```

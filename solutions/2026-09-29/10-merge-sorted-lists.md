# Merge Sorted Lists

**Difficulty:** Medium  
**Topic:** Linked List

Merge two sorted singly linked lists into one sorted list and return the head.

## Approach
Iteratively compare nodes and link the smaller one.

## Complexity
O(n+m) time, O(1) space

## Solution
```python
def merge_two_lists(l1, l2):
    dummy = prev = ListNode(0)
    while l1 and l2:
        if l1.val < l2.val:
            prev.next, l1 = l1, l1.next
        else:
            prev.next, l2 = l2, l2.next
        prev = prev.next
    prev.next = l1 or l2
    return dummy.next
```

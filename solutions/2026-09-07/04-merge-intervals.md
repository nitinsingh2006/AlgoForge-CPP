# Merge Intervals

**Difficulty:** Easy  
**Topic:** Sorting

Given a list of intervals represented as [start, end], merge all overlapping intervals and return the list of merged intervals.

## Approach
Sort intervals by start and merge sequentially.

## Complexity
O(n log n) time, O(n) space.

## Solution
```python
def merge(intervals):
    if not intervals: return []
    intervals.sort(key=lambda x: x[0])
    merged = [intervals[0]]
    for curr in intervals[1:]:
        last = merged[-1]
        if curr[0] <= last[1]:
            last[1] = max(last[1], curr[1])
        else:
            merged.append(curr)
    return merged
```

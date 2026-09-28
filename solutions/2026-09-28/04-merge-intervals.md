# Merge Intervals

**Difficulty:** Medium  
**Topic:** Sorting

Given a list of intervals, merge all overlapping intervals and return the list of merged intervals.

## Approach
Sort intervals by start, then iterate merging overlapping ones.

## Complexity
O(n log n) time, O(1) extra space (excluding output).

## Solution
```python
def solve(intervals):\n    if not intervals: return []\n    intervals.sort(key=lambda x:x[0])\n    merged=[intervals[0]]\n    for curr in intervals[1:]:\n        last=merged[-1]\n        if curr[0] <= last[1]:\n            last[1]=max(last[1],curr[1])\n        else:\n            merged.append(curr)\n    return merged
```

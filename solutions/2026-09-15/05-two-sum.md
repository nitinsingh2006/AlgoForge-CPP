# Two Sum

**Difficulty:** Easy  
**Topic:** Arrays

Find two indices in an array whose values sum to a target. Return the indices as a list. If no solution, return an empty list. Assume exactly one solution exists.

## Approach
Use a hash map to store numbers and their indices.

## Complexity
O(n) time, O(n) space

## Solution
```python
def two_sum(nums, target): d={};
 for i,n in enumerate(nums):
  if target-n in d:
   return [d[target-n], i]
  d[n]=i
 return []
```

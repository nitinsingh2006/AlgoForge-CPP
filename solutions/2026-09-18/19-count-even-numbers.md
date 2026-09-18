# Count Even Numbers

**Difficulty:** Easy  
**Topic:** Arrays

Given an array of integers, return the count of even numbers.

## Approach
Iterate through the array, increment a counter when the element is divisible by 2.

## Complexity
O(n) time, O(1) space

## Solution
```python
def count_even(nums): return sum(1 for x in nums if x%2==0)
```

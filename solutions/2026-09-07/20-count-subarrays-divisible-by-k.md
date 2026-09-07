# Count Subarrays Divisible by K

**Difficulty:** Hard  
**Topic:** Prefix Sum

Given an array of integers and an integer k, count the number of contiguous subarrays whose sum is divisible by k.

## Approach
Compute prefix sums modulo k and use a hash map to count equal remainders.

## Complexity
O(n) time, O(k) space

## Solution
```python
def solve(nums,k):
    count={0:1}
    prefix=0
    ans=0
    for num in nums:
        prefix=(prefix+num)%k
        ans+=count.get(prefix,0)
        count[prefix]=count.get(prefix,0)+1
    return ans
```

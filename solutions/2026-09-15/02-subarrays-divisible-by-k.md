# Subarrays Divisible by K

**Difficulty:** Medium  
**Topic:** Prefix Sum

Count the number of contiguous subarrays whose sum is divisible by a given integer K.

## Approach
Track prefix sums modulo K. For each remainder, the number of pairs of indices with same remainder gives subarrays divisible by K.

## Complexity
O(n) time, O(k) space

## Solution
```python
def subarrays_div_by_k(nums, k):
    from collections import defaultdict
    count = defaultdict(int)
    count[0] = 1
    pref = 0
    ans = 0
    for x in nums:
        pref = (pref + x) % k
        ans += count[pref]
        count[pref] += 1
    return ans
```

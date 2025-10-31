**Definition**
1. Define two ptrs, one at the left (`0`) and one at the right (`n-1`) of the array
2. Depending on the question, move one or both ptrs inward based on some condition
3. Continue until both ptrs meet or they cross
4. Left ptr is moved for larger values and right ptr is moved for smaller values

```Python
def two_ptrs(arr):
	l, r = 0, len(arr)-1
	
	while l < r:
		if condition_met:
			return result
		elif need_larger_value:
			l += 1
		else:
			r -= 1
```

**Algorithm Complexity**
Time: $O(n)$, since each ptr traverses the array at most once
Space: $O(1)$, since we're using only ptrs and no data structures

**Patterns**
- Sorted Array
- In-place modification
- Finding pairs/triplets





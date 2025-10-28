1. Define two ptrs that both start at the same position, left and right ptrs
2. Expand window by moving the right ptr (traversing array) and processing the new element
3. When a condition isn't met, shrink window by moving left ptr until condition is met again
4. Track the result using the current window size `r - l + 1`

```Python
def sliding_window(arr):
	l = 0
	res = 0
	for r in range(len(arr)):
		# expand window by doing smth
		
		# shrink window
		while condition_not_met:
			l += 1
		
		res = max(res, r-l+1)
	return res
```

**Algorithm Complexity**
- Time: $O(n)$ since each element is processed at most twice
- Space: 
	- $O(1)$ if we track variables
	- $O(k)$ if we track with hash map since at most `k` values in the hash map

**Patterns**
- Finding longest/shortest/maximum/contiguous subarray with one condition
- Looking for any consecutive elements (not any subset)

**Variations**
- Variable size window (with just ptrs)
- Variable size window (with hash map)
	- Used for counting character frequencies
- Fixed size window

**Additional Notes**
- `while` vs `if` for shrinking
	- Use `while` when condition can be violated by multiple elements
	- Use `if` when only one element can violate it




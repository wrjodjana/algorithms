**Definition**
1. Ensure that the array is sorted
2. Divide array into two halves and find the middle index `mid`
3. Compare middle element with our target value:
	- If `target` is larger then `mid`, than use right side to search (move `left` ptr)
	- if `target` is smaller then `mid`, than use left side to search (move `right` ptr)
	- if `target` equals `mid`, terminate process

```Python
def binary_search(arr, target):
	l, r = 0, len(arr)-1
	
	while l <= r:
		mid = (l + r) // 2
		if arr[mid] < target:
			l = mid + 1
		elif arr[mid] > target:
			r = mid - 1
		else:
			break
```

**Algorithm Complexity**
- Time: $O(\log n)$ since we're halving every iteration
- Space: $O(1)$ since we only use ptrs

**Patterns**
- Array is sorted
- Find exact element/value
- "Search for target" problems

**Additional Notes**
- Use `mid ± 1` with `while l <= r`, where we compare `mid` with`target`
- Use `l = mid` or `r = mid` with `while l < r`, where mid could be the answer

**Useful:**
https://leetcode.com/discuss/post/786126/python-powerful-ultimate-binary-search-t-rwv8/






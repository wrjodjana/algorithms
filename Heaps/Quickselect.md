**Quickselect**
- Goal: Finding kth smallest element in an unsorted array

1. Partition array by choosing pivot element, moving all values smaller on left of pivot and all values larger on right of pivot
	- Pivot should be chosen based on middle index (`l + (r-l) // 2`)
2. Compare pivot position to `k`
	- If pivot index is smaller then `k`, search right side of array
	- If pivot index is larger then `k`, search left side of array
3. Repeat until pivot index equals `k`

```Python
def quickselect(arr, k):
	l, r = 0, len(arr)-1
	
	while l <= r:
		pivot = partition(arr, l, r)
		
		if pivot == k:
			return arr[k]
		elif pivot < k:
			l = pivot + 1
		else:
			r = pivot - 1
```

Algorithm Complexity
- Time: 
	- $O(n)$ in average case
	- $O(n^2)$ in worst case where pivot value ends up at last and first elements continuosly
- Space: $O(1)$ iterative
1. Prefix sum is a new array that precomputes the sum of elements of all values previously
2. `prefix[i] = arr[0] + arr[1] + ... + arr[i]`
3. To find sum of subarray from index `l` to `r`: 
	- if `l == 0`: `prefix[r]`
	- Otherwise: `prefix[r] - prefix[l-1]`

```Python
def prefix_sum(arr):
	n = len(arr)
	
	prefix_sum = [0] * n
	prefix_sum[0] = arr[0]
	
	for i in range(1, n):
		prefix_sum[i] = prefix_sum[i - 1] + arr[i]
	
	return prefix_sum
```

**Algorithm Complexity**
- Time: $O(n)$ to build, $O(1)$ per query
- Space: $O(n)$ for prefix array

**Patterns**
- Problems asking for sum of elements from `i to j`
- Find subarrays with given sum
- Subarray sum equals k
- Multiple range sum queries on same array

**Additional Notes**
- Sometimes add `prefix[0] = 0` to avoid `l-1` edge case
- Can use hash map with prefix sums to count subarrays
- A dp algorithm used to find maximum sum of contiguous subarray (for 1D arrays)
- At any given point you have two choices for forming maximum sum subarray ending at i:
	- Start a new subarray from current element `nums[i]`
	- Extend previous maximum subarray by adding `nums[i]` to it
- Pick option that gives larger sum. This value is then compared to the global maximum

```Python
def maxSubArray(nums):
	curr, maximum = 0, float("-inf")
	
	for num in nums:
		curr = max(num, curr+num)
		maximum = max(maximum, curr)
	
	return maximum
```

**Algorithm Complexity**
- Time: $O(n)$ since single pass through array
- Space: $O(1)$ since we only use variables

**Patterns**
- Maximum/minimum sum subarray
- Problems asking for contiguous subarray with max/min property
- Buy/sell stock problems

**Additional Notes**
- Can be modified to track start/end indices of max subarray
- Works with negative numbers (unlike sliding window)
- If `curr` become negative, start fresh (greedy)




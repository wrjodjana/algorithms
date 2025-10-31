**Definition**
- Exploring possible paths until the end, then you backtrack (meaning you undo the last step)
- Imagine it's like a decision tree, where it starts with the empty array
- Components:
	- Base Case: when to save/return a solution
	- Choices: what options are available at each step
	- Constraints: what choices are valid/invalid
	- Backtracking step: Undo the choice to explore other paths

```Python
def backtrack(params):
	if base_case_condition:
		results.append(copy_of_sol)
		return
	
	for choice in choices:
		if violates_constraints:
			continue
		
		make_choice
		backtrack(updated_params)
		undo_choice
```

**Algorithm Complexity**
- Time: varies between questions
- Space: $O(n)$ for recursion depth + path storage

**Patterns**
- Generate all solutions
- Explore decision trees with multiple steps
- Constraints in question are also e.g. ($n \leq 20$)

**Additional Notes**
- Always copy the path using `path.copy()`
- If you can use duplicate values `backtrack(i)`, without: `backtrack(i+1)`
- Combinations: needs index `i`, as order doesn't matter, but we have to pick elements after
- Permutations: don't need index `i` as order matters so we check element every time



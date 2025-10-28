- Linear data structure that follows Last-in-First-out principle
- New elements are always pushed to the top and removal also happens at the top

```Python
stack = []

stack.append(30) # add 30 to top
stack.append(40) # add 40 to top
stack.append(50) # add 50 to top

stack[-1] # 50 is now at the top
stack.pop() # 50 is popped, 40 becomes new top
```

**Common Operations**
- `push(x)` - add to top - $O(1)$
- `pop()` - remove from top - $O(1)$
- `peek()` - view top without removing - $O(1)$
- `is_empty()` - check if empty - $O(1)$

**Algorithm Complexity**
- Time: $O(1)$ for all operations
- Space: $O(n)$ where `n` is no. of elements

**Patterns**
- Problems mention "last seen" or "most recent"
- Nested structures (brackets, parentheses)
- Need to process in reverse order

**Monotonic stack**
- Stack maintains elements in increasing or decreasing order
- Used for "Next greater/smaller element" problems
- Time: $O(n)$ since each element is pushed/popped once

**Additional Notes**
- Always check `if stack` before `pop()` or `stack[-1]`

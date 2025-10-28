**Definition**
- Exploring all nodes in the same level, before traversing the next level using the queue data structure

```Python
from collections import deque
def bfs(root):
	q = deque([root])
	while q:
		node = q.popleft()
		if node.left:
			q.append(node.left)
		if node.right:
			q.append(node.right)
```

**Algorithm Complexity**
- Time: $O(n)$ since we traverse through the node
- Space:
	- $O(w)$ where `w` is max width of tree
	- $O(n)$ for complete tree (worst case)

**Patterns**
- Level by level 
- Shortest path
- Min depth


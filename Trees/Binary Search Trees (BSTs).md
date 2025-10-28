**Definition**
- For any node in the tree, all of the left side has a smaller value then the node and all of the right side has a larger value then the node

```Python
def search(root, target):
	while root:
		if target < root.val:
			root = root.left
		elif target > root.val:
			root = root.right
		else:
			return root
```

**Algorithm Complexity**
- Time: $O(\log n)$ since we're searching half the tree in each step
- Space: $O(\log n)$ 

**Patterns**
- Use BST property to prune search (only go left OR right, not both)
- Find min/max of a tree
- Validate with range bounds (not just parent-child comparison)



**Definition**
- Exploring all nodes in a tree by going as deep as possible along each branch before moving to the next one

**Recursive**

```Python
def dfs(node):
	if not node:
		return
	
	dfs(node.left)
	dfs(node.right)
```
- Base case: when the node becomes `null`
- Recursive case: recurse on children

**Iterative**

```Python
def dfs(root):
	if not root:
		return
	
	stack = [root]
	while stack:
		node = stack.pop()
		if node.right:
			stack.append(node.right)
		if node.left:
			stack.append(node.left)
```
- Process nodes on right first, then left so left is processed first when popped


**Algorithm Complexity**
- Time: $O(n)$ since we traverse through every node
- Space: 
	- $O(h)$ where $h$ is height (recursion stack)
	- $O(n)$ for skewed tree (worst case)

**Traversals**

![[tree.png|275]]

Preorder Traversal
- Process node itself, then process left, then process right e.g. `[1, 2, 4, 5, 3, 10]`
- Use: Children needs information from parent or ancestors
- Passes: parameters down (accumulated sum, max so far, current path)

Inorder Traversal
- Process left, then process node and then process right e.g. `[4, 2, 5, 1, 10, 3]`
- Use: when tackling problems for BST where sorting matters

Postorder Traversal
- Process left, process right then process the node e.g. `[4, 5, 2, 10, 3, 1]`
- Use: Parent needs information from children to calculate something
- Return: Info that parent needs (height, sum, count)







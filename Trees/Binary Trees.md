**Definition**
- A binary tree has a two node references, its left and right children

```Python
class TreeNode:
	def __init__(self, val=0, left=None, right=None):
		root.val = 0
		root.left = None
		root.right = None
```

**Types**
- Complete Tree: Every level of tree is filled except last one
- Perfect Tree: Every level of tree is filled
- Full Tree: Every node has either 0 or 2 children (no nodes with 1 child)
- Balanced Tree: Height of left and right subtrees differ by at most 1 for every node
- Skewed Tree: Each parent has only 1 child

**Concepts**
- Depth: Distance from root to node (root depth = 0)
- Height of node: Distance from node to deepest leaf
- Height of tree: Height of root = max depth of any leaf




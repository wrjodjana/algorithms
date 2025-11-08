**Definition:**
- Quickly checking if two vertices are connected
- Parent node: direct parent node of a vertex
- Root node: a node without a parent node, can be viewed as the parent node itself

**Implementation:**
- `find` function finds the root node of a given vertex
- `union` function unions two vertices and makes their root nodes the same

**Union by Rank**
- Choose parent node based on the rank to limit maximum height of vertex
- Instead of always picking root of `x` or `y` as new root node, we choose the root node of the vertex with larger rank
- Then, merge the shorter tree under the taller tree and assign root node of taller tree as root node for both vertices

**Path Compression**
- Update parent node of all traversed elements to their root node
- Uses recursion to optimize the `find` function

**Implementation**
```Python
class UnionFind:
	def __init__(self, size):
		self.root = list(range(size))
		self.rank = [0] * size
	
	def find(self, x):
		if x == self.root[x]:
			return x
		return self.find(self.root[x])
	
	def union(self, x, y):
		rootX = self.find(x)
		rootY = self.find(y)
		
		if rootX != rootY:
			if self.rank[rootX] > self.rank[rootY]:
				self.root[rootY] = rootX
			elif self.rank[rootX] < self.rank[rootY]:
				self.root[rootX] = rootY
			else:
				self.root[rootY] = rootX
				self.rank[rootX] += 1
		
```

**Algorithm Complexity**
- Time:
	- `find`: $O(\alpha(n)) \approx O(1)$ 
	- `union`: $O(\alpha(n)) \approx O(1)$ 
- Space: $O(n)$ 
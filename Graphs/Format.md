**Array of Edges**
- Each element is of the form `[x,y]` which indicates there is an edge between x and y
- Pre-process input by using hash map where node is key and list of neighbors is value
- Example: `edges = [[0,1],[1,2],[2,0],[2,3]]`

```Python
def build_graph(edges):
	graph = defaultdict(list)
	for x, y in edges:
		graph[x].append(y)
		graph[y].append(x)
```

**Adjacency List**
- Nodes will be numbered from `0` to `n-1`, input is 2D integer array called `graph`
- `graph[i]` will be a list of all the outgoing edges from the `ith` node
- We can already access the neighbors of any given node, so no need preprocessing
- Example: `graph = [[1],[2],[0,3],[]]`, so 0 connects to 1, 1 connects to 2

**Adjacency Matrix**
- Nodes will be numbered from `0` to `n-1`, input is 2D matrix of size `n x n` called `graph`
- If `graph[i][j] == 1`, that means there is outgoing edge from node `i` to node `j`
- Two methods:
	- 1. During traversal, at any node iterate over `graph[node]` and if `graph[node][i] == 1`, then you know that node `i` is a neighbor
	- 2. Build hash map and then iterate over entire graph. If `graph[i][j] == 1`, then put `j` in the list associated with `graph[i]`
	- Time: $O(n^2)$ 

**Matrix**
- Input will be a 2D matrix and problem will describe story (e.g. each square represents smth)
- Each square `(row, col)` of the matrix is a node
- Neighbors are `(row-1, col)`,`(row, col-1)`, `(row+1, col)`, `(row, col+1)`


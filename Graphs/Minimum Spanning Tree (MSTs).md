**Definition:**
- A spanning tree is a connected subgraph in an undirected graph where all vertices are connected with the minimum number of edges
- An MST is a spanning tree with minimum possible total edge weight in a weighted undirected graph

**Cut Property**
- A cut is partition of vertices in a graph with two disjoint subsets
- A crossing edge is an edge that connects a vertex in one set with a vertex in another set
- Cut property is that for any cut `C` of the graph, if the weight of an edge `E` in the cut-set of `C` is strictly smaller than the weights of all other edges of the cut-set of `C` then this edge belongs to all MSTs of the graph

**Kruskal's Algorithm**
- Construct an MST:
1. Ascending sort all edges by their weight
2. Add edges in that order into the MST. Skip the edges that would produce cycles in the MST using disjoint set union
3. Repeat step 2 until `n-1` edges are added

**Prim's Algorithm**
- Construct an MST
1. Start with an arbitrary node in the MST
2. Select the minimum weight that connects a node in the MST to a node outside (use a min heap for the weights)
3. Mark nodes as visited when added to MST to avoid cycles
4. Continue until all `n` nodes are in the MST
 


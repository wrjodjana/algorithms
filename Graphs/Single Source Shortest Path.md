**Dijkstra's Algorithm**
- Take the starting point `u` as the center and gradually expand outward  while updating the shortest path to reach other vertices
- Each step selects the minimum weight from the currently reached vertices to find the shorts path to other vertices
- Only works with weights that are non-negative

**Implementation**
- Use a min heap to keep track of the smallest weights
- Use a visited set to keep track of all nodes that we have already visited previously
- Iterate through the next nodes to find the single shortest path

**Algorithm Complexity**
- Time: $O((V + E)\log V)$ 
- Space: $O(V)$

**Bellman-ford Algorithm**


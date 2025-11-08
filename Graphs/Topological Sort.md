**Definition:**
- Provides a linear sorting based on the required ordering between vertices in DAGs
- Given vertices `u` and `v`, to reach vertex `v` we must have reached vertex `u` first

**Kahn's Algorithm**
- Preprocess any courses that don't have any prerequisites (`indegree == 0`)
- Run BFS/DFS and check if any neighboring courses becomes complete
- Check if we then finished all of our courses

**Algorithm Complexity**
- Time: $O(V+E)$
- Space: $O(V+E)$




**Definition**
- A graph is a collection of nodes (vertices) and connections between those nodes (edges)
- $G = (V, E)$

**Types of Graphs**
- Undirected Graphs: edges between any two vertices do not have a direction, indicating a two way relationship
- Directed Graphs: edges between any two vertices is directional
- Weighted Graphs: each edge has an associated weight (e.g. time, distance, size)

**Graph Terminology**

![[graph.png|500]]

- Path: sequence of vertices to go through from one vertex to another (e.g. A to C is A,B,C). There can be multiple paths between two vertices
- Path length: number of edges in a path (e.g. A to C is path length 2)
- Cycle: a path where the starting point and endpoint are same vertex (e.g. A,B,D,F,E)
- Negative weight cycle: if sum of the weights of all edges of a cycle is a negative value
- Connectivity: if there exists at least one path between two vertices, these two vertices are connected
- Degree: the degree of a vertex is number of edges connecting to a vertex
- In-Degree: the number of edges that can be used to reach the node in directed graph
- Out-Degree: the number of edges that leaves a node in directed graph


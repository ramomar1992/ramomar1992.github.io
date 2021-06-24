# Graph Data Structure

Graphs is a non linear data structure used in many applications like GBS mapping and Social media networks. There is a lot to do with graphs. This is because of its efficiency and the wide range off applications we can use it in.

## some common terminology used when working with Graphs

1. Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
2. Edge - An edge is a connection between two nodes.
3. Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. Degree - The degree of a vertex is the number of edges connected to that vertex.

## Graph classifications

We can classify graphs according to many categories:

### Directed vs Undirected

1. Directed graphs are graphs that have arrows to determine the relationship between each vertex and its adjacent vertices. It is represented using multiple nodes with arrows between them as edges. The arrows mean that we can go from node one to node two but not vice versa if no opposite arrow is there.
2. Undirected are not represented using arrows, there is only lines between nodes and they mean that we can go on both directions from node one to two and from node two to one.

### Complete vs Connected vs Disconnected

1. Complete Graphs are ones that each node in the graph is connected to all other nodes in the graph. Which means that we can go from any node to all other nodes in just weight of 1.
2. Connected Graph is graph that has all of nodes have at least one edge. Looking closely at the different vertices of the graph, you will see that each node is connected to at least one other node or vertices. A Tree is a form of a connected graph.
3. A disconnected graph is a graph where some vertices may not have edges. Some nodes may not always be connected to other nodes or vertices of the graph. It is completely possible to have standalone nodes or edges (also known as islands) in a graph data structure.

### Acyclic vs Cyclic

1. Acyclic Graph is a directed graph without cycles. A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.
2. A Cyclic graph is a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertex.

## Graph Representation

A sparse graph is when there are very few connections. a dense graph is when there are many connections.
There are many ways in which we can represent the graphs.

* Edge List: Which is a list that contains all individual edges represented as pairs of keys and values.
* Adjacency Matrix: An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix. Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection. For undirected graphs, the matrix will always be symmetric.
* An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected. Adjacency lists make it easy to view if one vertices connects to another.

## Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.

When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. If there is not a connection between the two vertices, you can put a 0, although it is known for some people to put the infinity sign instead.

Within adjacency lists, you must include both the weight and the name of the adjacent vertex. A great way to represent the {vertices, weight} connection is through some sort of key/value pair data structure.

## examples of graphs in use

* GPS and Mapping
* Driving Directions
* Social Networks
* Airline Traffic
* Netflix uses graphs for suggestions of products

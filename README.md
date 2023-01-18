# DAA-CIA-1---Abhishek-Herbert-Samuel-B.Tech-CSE-IoT-A-21011102004
For the given graph , one can use Prim's and Kruskal's Algorithm as the minimum spanning tree is generated in the first iteration itself with a total minimum cost of 8. Dijkstra's can also be used to generate the shortest paths (NOT THE MST)with a higher total cost of 16 and individual path cost due to its cumulative nature of calculation of costs using the source node.Also , from the given source node A , a path exists to reach all other nodes B,C,D and E. However, one cannot use these 3 algorithms in general as a path need not always be generated ( for example, if D was the source node here then there would be no possible way to generate the MST or find the shortest path using Dijkstra's algorithm as no path exists to reach the other nodes from D.) Also, while the negative weight here from E to D of cost -5 was not a factor in the calculation process due to the nature of the question, this need not be the case for all graphs of a similar type.In fact, Prim's and Kruskal's work in all cases with only undirected graphs with weights >=0 and Dijkstra's works with directed graphs but without any negative weights.

The MST using Prim's and Kruskal's is below for the given graph:
A->C->B->E/D(can go to either E or D from B) with a total cost of 8.

The shortest paths from the source node A to all other nodes using Dijkstra's is below.

A->C->B (COST 3)

A->C (COST 2)

A->C->B->D(COST 5)

A->C->B->E (COST 6)

Here the total cost is 16.

The required adjacency matrix for the given graph is:

[ 0 4 2 0 0

0 0 3 2 3

0 1 0 4 5

0 0 0 0 0

0 0 0 -5 0 ]

I have used the C programming language for all 3 programs as it is faster and more efficient in comparison to Python/Java /C++ and I am familiar with it the most as I learnt data structures using the C language.
Regarding the performance of the 3 algorithms, Prim's is more effective for dense graphs while Kruskal's is faster for sparse graphs. The time complexity of Prim's algorithm is O(V^2). The time complexity of Kruskal's algorithm is O(E log V) where V is the number of vertices and E is the number of edges.
The time complexity of Dijkstra's algorithm is O(V^2). It is similar to Prim's algorithm in terms of it's algorithmic implementation and time complexity.

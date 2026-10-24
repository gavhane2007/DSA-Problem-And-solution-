# Modified Prim's Algorithm for Fiber-Optic Network in C++

## 1. Problem Statement

To develop a modified C++ program to represent offices as vertices and possible fiber-optic cable connections as weighted edges. Apply Prim's algorithm to connect all offices with the minimum total cable cost. The program allows users to update an existing edge weight and recalculate the minimum spanning tree. It displays every selected edge with its weight and running total cost. It also detects disconnected graphs and reports whether a spanning tree can be formed.

## 2. Approach

1. Represent each office as a vertex and each possible fiber-optic connection as a weighted edge.
2. Store the connection costs in a weighted adjacency matrix.
3. Initialize all offices as unvisited and select the first office as the starting vertex.
4. Apply Prim's algorithm to find the minimum spanning tree of the network.
5. Select the minimum-weight edge connecting a visited office to an unvisited office.
6. Display each selected edge, its weight, and the running total cable cost.
7. Check whether all offices are connected. If no valid edge is available before all offices are visited, report that the graph is disconnected and a spanning tree cannot be formed.
8. Ask the user to select two offices and enter the updated cable connection weight.
9. Update the corresponding edge weight in both directions of the adjacency matrix.
10. Apply Prim's algorithm again to calculate the updated minimum spanning tree.
11. Display the updated selected edges, their weights, the running total cost, and the final minimum cable cost.
12. Report whether a spanning tree can be formed for the updated network.

## 3. Complexity Analysis

Let:
- `V` = number of offices (vertices).
- `E` = number of possible fiber-optic connections (edges).

### Time Complexity

| Operation | Complexity |
|---|---|
| Initialize the visited array | O(V) |
| Create and read the adjacency matrix | O(V²) |
| Find the minimum-weight edge using Prim's algorithm | O(V³) |
| Update an edge weight | O(1) |
| Detect a disconnected graph | Included in Prim's algorithm |
| Recalculate the minimum spanning tree after an update | O(V³) |

**Overall Time Complexity:** O(V³) per execution of Prim's algorithm. Since the modified program executes Prim's algorithm before and after updating an edge, the overall asymptotic time complexity remains O(V³).

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Store the adjacency matrix | O(V²) |
| Maintain the visited array | O(V) |
| Display selected edges and running cost | O(1) additional space |
| Update an edge weight | O(1) |

**Overall Space Complexity:** O(V²), because the adjacency matrix stores the connection costs between offices.

## 4. Conclusion

The modified Fiber-Optic Network project demonstrates the practical implementation of Prim's algorithm in C++. It finds the minimum-cost connections required to connect all offices and displays each selected edge with its weight and running total cost. The program allows users to update an edge weight and recalculate the minimum spanning tree. It also detects disconnected graphs and determines whether a spanning tree can be formed. This project demonstrates graph representation, greedy algorithms, minimum spanning trees, dynamic edge-weight updates, and time and space complexity analysis.

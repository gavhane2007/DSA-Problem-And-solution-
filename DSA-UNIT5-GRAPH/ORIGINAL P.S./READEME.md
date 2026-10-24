# Fiber-Optic Network Using Prim's Algorithm in C++

## 1. Problem Statement

To develop a C++ program to represent offices as vertices and possible fiber-optic cable connections as weighted edges. Apply Prim's algorithm to connect all offices with the minimum total cable cost. The program displays the selected edges, their weights, and the running and final total cost. The modified program also allows users to update an edge weight and recalculate the minimum spanning tree. It detects disconnected graphs and reports whether a spanning tree can be formed.

## 2. Approach

1. Represent each office as a vertex and each possible fiber-optic connection as a weighted edge.
2. Store the connection costs in a weighted adjacency matrix.
3. Initialize all offices as unvisited and select the first office as the starting vertex.
4. Apply Prim's algorithm to select the minimum-weight edge connecting a visited office to an unvisited office.
5. Mark the newly connected office as visited and update the total cable cost.
6. Display every selected edge, its weight, and the running total cost.
7. Continue until all offices are connected or no valid edge is available.
8. If all offices are connected, display the minimum total cable cost. Otherwise, report that the graph is disconnected and a spanning tree cannot be formed.
9. In the modified program, allow the user to update an edge weight in the adjacency matrix.
10. Apply Prim's algorithm again to calculate and display the updated minimum spanning tree and total cable cost.

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
| Update an edge weight in the adjacency matrix | O(1) |
| Check whether a spanning tree can be formed | Included in Prim's algorithm |
| Run Prim's algorithm again after updating an edge | O(V³) |

**Overall Time Complexity:** O(V³) per execution of Prim's algorithm. The modified program runs the algorithm twice, but its overall asymptotic time complexity remains O(V³).

### Space Complexity

| Operation | Auxiliary Space |
|---|---|
| Store the adjacency matrix | O(V²) |
| Maintain the visited array | O(V) |
| Store selected edge information | O(1) if displayed immediately |
| Update an edge weight | O(1) |

**Overall Space Complexity:** O(V²), because the adjacency matrix requires quadratic space to store the connection costs between offices.

## 4. Conclusion

The Fiber-Optic Network project demonstrates the implementation of Prim's algorithm in C++. It identifies the minimum-cost connections required to connect offices and displays the selected edges with their weights and running total cost. The modified program supports edge-weight updates and recalculates the minimum spanning tree. It also detects disconnected graphs and determines whether all offices can be connected. This project demonstrates the practical application of graphs, adjacency matrices, greedy algorithms, minimum spanning trees, and time and space complexity analysis.

# A_Star

The A* algorithm is a popular pathfinding algorithm used to find the shortest path between two nodes in a graph. It takes into account the cost to reach each node and an estimate of the remaining cost to reach the goal. Here's how the A* algorithm works:

1. The `Graph` class is defined, which takes an adjacency list (`adjac_lis`) as input during initialization.
2. The `get_neighbors` method returns the neighbors of a given node.
3. The `h` method defines the heuristic function, which returns the heuristic value (h-score) for a given node.
4. The `a_star_algorithm` method implements the A* algorithm to find the shortest path between the `start` and `stop` nodes.
5. The algorithm maintains the `open_lst` (nodes to be visited), `closed_lst` (visited nodes), `poo` (cost from start to each node), and `par` (parent node for each node) data structures.
6. The algorithm iterates until the `open_lst` is empty.
7. It selects the node `n` with the lowest f-score (`poo[n] + h(n)`) from the `open_lst`.
8. If `n` is the goal node (`stop`), it reconstructs the path by following the parent nodes in the `par` dictionary and returns the path.
9. Otherwise, it explores the neighbors of `n`, updates their costs (`poo`), and adds them to the `open_lst` if necessary.
10. The algorithm continues until either the goal node is reached or there are no more nodes to explore.
11. If the goal node is not reached, it prints a message indicating that the path does not exist.
12. In the provided example, an instance of the `Graph` class is created with the given adjacency list (`adjac_lis`), and the A* algorithm is applied to find the shortest path between nodes 'A' and 'D'.

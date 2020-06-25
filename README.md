# Deivery
Delivery problem that require TSP
The problem require to find the minimum distance for visiting all the positions, knowing that the delivery speed changes from a city to another.
You are given a weighted complete graph where nodes are the positions and the weight of an edge connecting two nodes is the Euclidean distance separating those nodes. Problem asks to find the minimum velocity so that a Hamiltonian path exists.
The main difficulty of this problem is to determine the order of nodes to visit first. You can try all possible ways (generating all permutations of n elements) but this will timeout as the complexity is O(n!).
The idea here is to use Binary search with Held–Karp dynamic programming solution to TSP: for a given velocity check if a Hamiltonian path exists in O(n².2^n). Your objective is to minimize the time at which you will reach each node.
Final complexity O(log(Vmax).n².2^n) where Vmax is an arbitrary large velocity at which a Hamiltonian path can be found.

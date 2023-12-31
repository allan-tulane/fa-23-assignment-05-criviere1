# CMPS 2200 Assignment 5
## Answers

**Name:** Collette Riviere


- **1a.** Since each node has d children, the max depth of a d-ary heap with n (also |V|) nodes is log_d (|V|).


- **1b.** Work of insert is O(log_d |V|). Work of delete-min is O(d*log_d |V|).


- **1c.** |V|*(d*log_d |V|) + (|V|+|E|)*(log_d |V|) = (log_d |V|)*(|V|*d + |E|)

The work for Dijkstra's algorithm with a d-ary heap, the work is O((log_d |V|)*(|V|*d + |E|)).


- **1d.** If d = |E| / |V|, then the work becomes O((log|V| / log(|E|/|V|)) * (|V|*|E|/|V| + |E|)) = O((log|V| / log(|E|/|V|)) * (2|E|)). In the case where |E| dominates, then the runtime reduces to O(|E|).


- **2a.** 
APSP(0,1,0) = -2
APSP(0,1,1) = -2
APSP(0,1,2) = 3

APSP(0,2,0) = 2
APSP(0,2,1) = -1
APSP(0,2,2) = 2

APSP(1,2,0) = 0
APSP(1,2,1) = 1
APSP(1,2,2) = 1


- **2b.** APSP(i,j,1) = APSP(i,1,1) + APSP(1,2,1) + APSP(2,j,j). 

          APSP(i,j,2) = APSP(i,2,2) + APSP(2,1,2) + APSP(1,0,1) + APSP(0,j,0)


- **2c.** The optimal substructure for APSP(i,j,k) is if k in the shortest path from i to j, then that shortest path from i to j is a combination of the shortest path between i and k, and k and j.


- **2d.** Using memoization, |V|^3 distinct subproblems will be calculated. The resulting work of the approach is O(|V|^3).


- **2e.** Johnson's Algorithm has O(|V|*|E|*log|E|) work. The dynamic programming algorithm is preferable for dense graphs, where Johnson's algorithm blows up due to the large number of edges.


- **3a.** Yes, any MST solution will be a solution to MMET. If you have a graph G, you can have multiple spanning trees. If you take the MET and call the maximum weight B, then any other spanning tree with that edge weight B, will be a MMET. But it may or may not be a MST because the total edge weight might be bigger than the original MST or might be equal to the original MST.


- **3b.** The next best tree will probably only differ from the MST by only one edge. So we need to find an edge e' that is not in the MST and replace it for an edge, e, currently in the MST. This should still result in a spanning tree and the weight difference is a minimum. 


- **3c.** The optimal MST can be found with Kruskal's algorithm (O(|E| log|E|)). Then for each edge in the MST, temporarily exclude it from the edge list then try to find a MST with the remaining edges (O(|E|^2 log|E|)). Whichever tree gives the minimum weight difference will be the second best tree (O(|E|)). The total work is O(|E|^2 log|E|).

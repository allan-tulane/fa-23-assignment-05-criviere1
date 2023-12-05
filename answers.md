# CMPS 2200 Assignment 5
## Answers

**Name:** Collette Riviere


- **1a.** Since each node has d children, the max depth of a d-ary heap with n (also |V|) nodes is log_d (|V|).


- **1b.** Work of insert is O(log_d |V|). Work of delete-min is O(d*log_d |V|).


- **1c.** |V|*(d*log_d |V|) + (|V|+|E|)*(log_d |V|) = (log_d |V|)*(|V|*d + |E|)

The work for Dijkstra's algorithm with a d-ary heap, the work is O((log_d |V|)*(|V|*d + |E|)).


- **1d.** If d = |E| / |V|, then the work becomes O((log|V| / log(|E|/|V|)) * (|V|*|E|/|V| + |E|)) = O((log|V| / log(|E|/|V|)) * (2|E|)). In the case where |E| dominates, then the runtime reduces to O(|E|).


- **2a.** 
APSP(0,1,2) = 3  ## ?? idk if any of these are right
APSP(1,0,2) = 3
APSP(0,2,1) = -1
APSP(2,0,1) = -1
APSP(1,2,0) = 0
APSP(2,1,0) = 0


- **2b.** APSP(i,j,1) = -1 and APSP(i,j,2) = 3


- **2c.**


- **2d.**


- **2e.**


- **3a.**


- **3b.**


- **3c.**

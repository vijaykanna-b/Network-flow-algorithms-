# Network-flow-algorithms-FORD FULKERSON METHOD FOR SOLVING MAXIMUM FLOW

STATEMENT : Given a graph which represents a flow network where every edge has a capacity. Also given two vertices source "s" and sink "t" in the graph, find the maximum possible flow from s to t with the following constraints:
->we call it a method rather than algorithm because it encompasses several implementations with differing running times. implement with 3 different algorithms.


PROBLEM EXPLANATION: An augmenting path is a simple path from source to sink which do not include any cycles and that pass only through positive weighted edges. A residual network graph indicates how much more flow is allowed in each edge in the network graph. If there are no augmenting paths possible from S to T, then the flow is maximum. The result i.e. the maximum flow will be the total flow out of source node which is also equal to total flow in to the sink node.

BOTTLENECK CAPACITY: It decides the maximum possible flow from source to sink through any augmented path.

RESIDUAL CAPACITY: Its original capacity of edge minus flow

RESIDUAL GRAPH: Adds the additional possible flow. If there is such a path from source to sink then there is a possibility to add flow.


ALGORITHM 1:

Start with initial flow as 0
While there is an augmented path from source to sink add the path flow to flow.
Return flow.


ALGORITHM 2: 
    
    Ford Fulkerson(Graph G, Node S, Node T):
    
    Initialise flow in all edges to 0
    
    while (there exists an augmenting path(P) between S and T in residual network graph):
    
        Augment flow between S to T along the path P
        
        Update residual network graph
        
    return

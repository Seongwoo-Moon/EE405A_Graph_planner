# EE405A_Graph_planner
EE405A Graph planner


This repository contains code for EE405A basic graph planner using the results of https://github.com/Guri-cccc/node_link_generator_ee405.git. 
Explanation:
- Load CSV file and generate node links.
- Set the start node as the closest node from the current global position.
- Set the goal node as the closest node among mine nodes.
- Run Dijkstra's algorithm.
- Publish the global path (of type nav_msgs::Path).
- Upon arrival, change the node status to visited=true.
- Use the global path in the control space planner.
  
### Launch command

```
roslaunch graph_planner graph_planner.launch
```

### Topic

- /graph_planner/path/global_path : The results of graph planning.
- /graph_planner/marker/nodes_text : ID of each node
- /graph_planner/marker/edges : Edges of graph


In [[Godot]], **NavigationRegion3D** is a traversable 3D region based on a [[NavigationMesh]] that [[NavigationAgent3D|NavigationAgent3Ds]] can use for pathfinding.

Two regions can be connected to each other if they share a similar edge. You can set the minimum distance between two vertices required to connect two edges by using `NavigationServer3D.map_set_edge_connection_margin()`

Overlapping two regions navigation meshes is no enough for connecting two regions. They must share a similar edge. The cost of entering this regions from another region can be controlled with the ``enter_cost`` value
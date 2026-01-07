The distance threshold before a path point is considered to be reached. This allows agents to not have to hit a path point on the path exactly, but only to reach its general area.

If this value is set too high, the [[NavigationAgent3D]] will skip points on the path, which can lead to it leaving the [[NavigationMesh]]. 

If this value is set too low, the [[NavigationAgent3D]] will be stuck in a repath loop because it will constantly overshoot the distance to the next point on each physics frame update.

```Javascript
void set_path_desired_distance(value: float)
float get_path_desired_distance()
```
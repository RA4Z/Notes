In [[Godot]], **CanvasLayer** is a node used for independent rendering of objects within a 2D scene.

[[CanvasItem]]-derived nodes that are direct or indirect children of a **CanvasLayer** will be drawn in that layer. The layer is a numeric index that defines the draw order. The default 2D scene renders with index `0`, so a **CanvasLayer** with index `-1` will be drawn below, and a **CanvasLayer** with index `1` will be drawn above.

Each **CanvasLayer** is drawn on one specific [[Viewport]] and cannot be shared between multiple [[Viewport|Viewports]].
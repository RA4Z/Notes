In [[AnimationTree]], `BlendSpace2D` is a node to do advanced blending in two dimensions. Points representing animations are added to a 2D space and then a position between them is controlled to determine the blending:
![[animtree_blendspace2d.gif]]

You may place these points anywhere on the graph by right clicking or using the **add point** button, whose icon is a pen and point. Wherever you place the points, the triangle between them will be generated automatically using Delaunay. You may also control and label the ranges in X and Y.
![[animtree_blendspacepoints.gif]]

Finally, you may also change the blend mode. By default, blending happens by interpolating points inside the closest triangle. When dealing with 2D animations (frame by frame), you may want to switch to _Discrete_ mode. Alternatively, if you want to keep the current play position when switching between discrete animations, there is a _Carry_ mode. This mode can be changed in the _Blend_ menu:
![[animtree_blendmode.webp]]

BlendSpace1D works just like BlendSpace2D, but in one dimension (a line). Triangles are not used
![[animtree_blendspace1d.webp]]

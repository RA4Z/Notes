In [[Godot]], **GridMap** lets you place meshes on a grid interactively. It works both from the editor and from scripts, which can help you create in-game level editors.

GridMaps use a [[MeshLibrary]] which contains a list of tiles. Each tile is a mesh with materials plus optional collision and navigation shapes.

A GridMap contains a collection of cells. Each grid cell refers to a tile in the [[MeshLibrary]]. All cells in the map have the same dimensions
In [[Godot]], it's possible to access paths using `res://` and `user://`
[File paths in Godot projects — Godot Engine (stable) documentation in English](https://docs.godotengine.org/en/stable/tutorials/io/data_paths.html)

### Project Folder `res://`
[[Godot]] considers that a project exists in any folder that contains a `project.godot` text file, even if the file is empty. The folder that contains this file is your project's root folder.

You can access any file relative to it by writing paths starting with `res://`, which stands for resources. For example, you can access an image file `character.png` located in the project's root folder in code with the following path: `res://character.png`.

### User Data `user://`
To store persistent data files, like the player's save or settings, you want to use `user://` instead of `res://` as your path's prefix. This is because when the game is running, the project's file system will likely be read-only.

The `user://` prefix points to a different directory on the user's device. Unlike `res://`, the directory pointed at by `user://` is created automatically and _guaranteed_ to be writable to, even in an exported project.

By default, the `user://` folder is created within [[Godot]]'s editor data path in the `app_userdata/[project_name]` folder.

On HTML5 exports, `user://` will refer to a virtual filesystem stored on the device via IndexedDB. (Interaction with the main filesystem can still be performed through the [JavaScriptBridge](https://docs.godotengine.org/en/stable/classes/class_javascriptbridge.html#class-javascriptbridge) singleton.)
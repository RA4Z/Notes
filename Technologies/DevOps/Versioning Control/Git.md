Git is a free, open-source **distributed version control system** designed to track changes in files, especially source code, and facilitate collaboration among developers.

Git allows multiple developers to work on a project simultaneously, even offline, by maintaining a complete local copy of the project and its history.

It stores data as [[Snapshot|snapshots]] of the project rather than as a series of file-based changes, making it efficient and reliable.

Git organizes data into three primary types of objects **blobs**, **trees** and **commits**

- **Blobs** store the content of the files in your repository. Each version of a file is represented by a blob object, which is identified by a unique hash
- **Trees** represent the directory structure of your project. They act as pointers that link tree objects with blobs, establishing relationships between files and folders
- **Commits** are the metadata associated with each [[Snapshot]]. Each commit points to a tree object, representing the directory structure at that commit

When a commit is created, Git constructs a tree object that represents the state of all files
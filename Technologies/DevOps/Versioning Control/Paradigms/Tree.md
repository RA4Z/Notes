In [[Git]], a tree is a core object that maps file names and permissions to their corresponding [[Blob]] objects, representing a directory [[Snapshot]] at a specific point in time.

Every commit in Git points to a **root tree**, which recursively references other trees (subdirectories) and [[Blob|blobs]] (file contents). This structure allows [[Git]] to reconstruct the exact state of a project for any commit

- **Storage**: Trees are stored in ``.git/objects/``and identified by their [[SHA-1 hash]]
- **Creation**: Built from the staging area (``.git/index``) during ``git commit``
- **Reuse**: Identical trees are reused across commits to save space
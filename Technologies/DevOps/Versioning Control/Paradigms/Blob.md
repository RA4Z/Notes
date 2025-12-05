Binary Large Object is a collection of binary data stored as a single entity. 

A blob is file's binary data, stored along with the size of that data and a label indication the object's type, which is 'blob'

- **Blobs** are used to store the contents of files in a Git repository
- They are stored in the ``.git/objects/`` directory and are named using their SHA-1 hash
- GitHub's REST API allows you to create and retrieve blobs programmatically
A git Snapshot is a representation of your project at a specific moment

### Basic Workflow about creating a Snapshot
- **Stage changes**
```Powershell
git add file.txt
```

- **View staged/unstaged changes**
```Powershell
git status
git diff # unstaged changes
git diff --staged # staged changes
```

- **Commit the snapshot**
```Powershell
git commit -m "Describe changes"
```

### Inspecting Snapshots
You can compare snapshots or retrieve specific file states:
```Powershell
# Compare working directory with a branch snapshot
git diff branch_name
# Restore a file from a specific snapshot
git checkout <commit_hash> -- file.txt
# View commit history (snapshots)
git log --oneline
```

### Under the Hood
Git stores snapshots as **objects** in `.git/objects`. Each object is identified by a [[SHA-1 Hash]]:
```Powershell
echo "Hello" | git hash-object -w --stdin
git cat-file -p <hash>
```

### Key Takeaways
- Commit = Snapshot + [[Metadata]]
- Snapshots make branching, merging and reverting efficient
- Git's garbage collection `git gc` compacts snapshots into packfiles to save space
In [[Git]], Commit is a [[Snapshot]] of your project at a specific point in time, recording changes along with a descriptive message. Helping maintain a clear project history and allows you to revert or review changes easily

### Stage and Commit Changes
- **Stage files** you want to include in the commit: `git add file1.txt file2.txt` To stage all changes: `git add .`
- **Create the commit** with a message:
```Powershell
  git commit -m "Describe your changes here"
  ```

### Write Detailed Multi-line Messages
Run `git commit` without `-m` to open your default editor:
- First line: short summary (≤50 characters)
- Blank line
- Detailed explanation of changes

### Amend the Last Commit
To add forgotten changes or fix the last commit message:
```Powershell
git add missed_file.txt
git commit --amend -m "Updated commit message"
```

### Best Practices
- Keep commits **small and focused**
- Use **imperative mood** in messages (e.g., "Add feature" not "Added feature")
- Commit often to maintain a clear history
- Use ``git log --oneline`` to review recent commits

### Multi-line Tip
Run `git commit` with -m "" -m "" to create a title and a description of your commit
```Powershell
git commit -m "Commit Title" -m "Commit Description"
```
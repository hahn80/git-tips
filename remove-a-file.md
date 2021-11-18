# Remove a file form history

1. Exclude the from in gitignore

2. Remove the file from history:
```
git filter-branch --tree-filter 'rm -f /path/to/sensitive/file' HEAD
```

3. Update the history to remote:
```
git push origin --force --all
```

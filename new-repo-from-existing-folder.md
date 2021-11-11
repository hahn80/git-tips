# Create a new repository from an existing folder

1. Init the local git:
```
git init
```

2. Create a remote repo:
```
gh repo create project-name -d "Description for project-name" --public
```

3. Update the changes when created the new repo:
```
git pull --set-upstream origin main 
```

4. Edit files, add, commit and upload to github:
```
git add .
git commit -m "Commit description"
git push origin HEAD:main
```

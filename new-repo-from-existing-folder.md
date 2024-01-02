# Create a new repository from an existing folder

1. Init the local git:
```
cd existing_folder/
git init
```

2. Default branch is master! We need to change it!

```
git branch -m main
```

4. Create a remote repo:
```
gh repo create project-name -d "Description for project-name" --public
```

3. Update the changes when created the new repo:
```
git checkout main
git pull
```

4. Edit files, add, commit and upload to github:
```
git add .
git commit -m "Commit description"
git push
```

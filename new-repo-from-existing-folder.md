# Create a new repository from an existing folder

## For public repos:

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

## For private repos

For a private repository:

1. Create a remote repo:

```sh
gh repo create project-name -d "Description for project-name" --private
```

2.a Create a new repository on the command line

```sh
echo "# Project Title" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:hahn80/project-name.git
git push -u origin main
```


2.b Push an existing repository from the command line

```sh
git remote add origin git@github.com:hahn80/project-name.git
git branch -M main
git push -u origin main
```

Now you can set config, add, commit and push.

Notice: set url to remote:
```sh
git remote set-url origin git@github.com:hahn80/project-name.git
git push --set-upstream origin main
```


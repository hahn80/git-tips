# Handle branches

1. List all branches:

```sh
git branch -a
```

2. Check out a branch:

```sh
git checkout main
```

3. Delete a branch locally:

```sh
git branch -d master
```

4. Delete a branch remotely:

```sh
git push origin -d master
```

5. Merge all files from master to main:

```sh
git:(master) git branch main
git:(master) git checkout main
git:(main) git pull origin master
git:(main) git checkout master
git:(master) git pull

git pull --rebase
git push --set-upstream origin main
# if get a rejected error, continue to push #
git push -f origin main
# Now delete master branch local/remote #
git branch --remotes --delete origin/master
git push origin --delete master
```

6. Check out all submouldes:

```sh
git submodule update --init --recursive
```


## Working with multiple git accounts

1. Check out ssh config file (`~/.ssh/config`) to see git accounts:

```shell
	git@github.com:hahn80/project.git => user is hahn80
	git@github.texervn:texervn/project.git => user is texervn
```

## Clone another git to mine

```shell
	git clone https://github.com/githubtraining/hellogitworld
	cd hellogitworld
	git config user.email texervn@email
	git config user.name "Texer VN"
	git remote set-url origin git@github.texervn:texervn/hellogitworld.git
```

## Clone my repository via SSH

```shell
	git clone git@github.texervn:texervn/hellogitworld.git
	cd hellogitworld
```


## Push a local git folder to github

```shell
	cd /path/to/project
	git config user.email "hahn80@email"
	git config user.name  "Hahn 80"
	git remote set-url origin git@github.com:hahn80/project.git
	git push
```

## Push a non-git folder to github

```shell
	cd /path/to/project
	git init
	git config user.email "hahn80@email"
	git config user.name  "Hahn 80"
	git remote set-url origin git@github.com:hahn80/project.git
	git add .
	git commit -m "Initial commit"
	git push --set-upstream origin master
```

## Use gh client to create a repository

First, switch to a right account:

```shell
	gh auth switch
```

Now, create a repository and clone to local

```shell
	gh repo create project --add-readme -d "Sample Project" -l MIT --public --clone
	cd project
	git status
	git config user.email
	git config user.name
```

If we want to create a private repository, just use --private inplace of --public

# Create a new repository from terminal

0. Login to github using gh command:

```
gh auth login
```

If we are using ssh and have authenticated already, just select the right account before creating a project.

```
gh auth switch
```


1. Create a repo named: myproject:
```
gh repo create myproject --add-readme -d "Description of my project" -l GNU --public --clone
```

Or use the silent mode:
```
gh repo create myproject -y --add-readme -d "Description of my project" -g Python -l gpl-3.0 --public --clone
```

2. Update the changes from myproject:
```
cd myproject/
git pull
```

3. Edit files, add, commit and upload to github:
```
git add .
git commit -m "Commit description"
git push
```

Notes: Repeat step 2) and 3) updating new changes.

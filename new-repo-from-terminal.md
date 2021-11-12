# Create a new repository from terminal

0. Login to github using gh command:
```
gh auth login
```

1. Create a repo named: myproject:
```
gh repo create myproject -d "Description of my project" --public
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
```
git push origin HEAD:main
```

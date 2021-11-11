# Manage collabotators to your repository

1. Invite *username* to your repo:
```
gh api -X PUT repos/hahn80/myproject/collaborators/username -f permission=push
```

2. Remove *username* from your repo:
```
gh api -X DELETE repos/hahn80/myproject/collaborators/username
```

Notes: permission could be pull; push; admin



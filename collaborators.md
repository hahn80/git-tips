# Manage collabotators to your repository



## Working on a shared project

Assuming this is a **shared project** where you have direct push access, here's the standard workflow using Git from the command line.


### 1. Clone the Repository

```bash
git clone https://github.com/hahn80/staport.git
cd staport
```

### 2. Fetch the Latest Changes

Always start with an up-to-date local copy:

```bash
git pull origin main
```

### 3. Create and Switch to a New `dev-001` Branch

Create a branch named `dev-001`:

```bash
git checkout -b dev-001
```

This creates the branch and switches to it, based on the current branch (usually `main`).

### 4. Make Your Changes
- Edit files using your code editor.
- Add new files if needed.

### 5. Stage and Commit Your Changes

```bash
git add .
git commit -m "Your descriptive commit message here"
```

Commit often with clear messages.

### 6. Push the Branch to GitHub

Push your new `dev-001` branch to the remote repository:
```bash
git push origin dev-001
```

- If it's the first push for this branch, you can use `git push -u origin dev-001` to set upstream tracking.
- GitHub will often output a URL to create a pull request directly after this command.

### 7. Create a Pull Request (PR) on GitHub

- Go to the repository on GitHub.com.
- You'll likely see a banner saying "Your recently pushed branch: dev-001" with a **Compare & pull request** button. Click it.
- Alternatively:
  - Click **Pull requests** tab > **New pull request**.
  - Set **base branch** to `main` (or whatever the target is).
  - Set **compare branch** to `dev`.
  - Click **Create pull request**.
- Add a title and description explaining your changes.
- Assign reviewers if needed.
- Click **Create pull request**.

### 8. Additional Tips

- **After PR is merged**: Delete the branch on GitHub (it offers a button), then locally:

  ```bash
  git checkout main
  git pull
  git branch -d dev-001
  ```
  
- **Via GitHub Web UI (no CLI)**: You can create a branch directly on GitHub, edit files online, and commit – GitHub will prompt to create a PR automatically.



## Advanced CMD


1. Invite *username* to your repo:
```
gh api -X PUT repos/hahn80/myproject/collaborators/username -f permission=push
```

2. Remove *username* from your repo:
```
gh api -X DELETE repos/hahn80/myproject/collaborators/username
```

Notes: permission could be pull; push; admin



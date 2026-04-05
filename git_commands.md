# Industry-Level Git & GitHub Commands Practice

---

## 1. Git Configuration Commands

### `git config --global user.name`
-**Purpose:** Sets your name globally for all Git commits.
- **Syntax:** `git config --global user.name "Your Name"`
- **Example:**
```
git config --global user.name "NIKHILA"
```

---

### `git config --global user.email`
- **Purpose:** Sets your email globally for all Git commits.
- **Syntax:** `git config --global user.email "you@example.com"`
- **Example:**
```bash
git config --global user.email "n220017@example.com"
```

---

### `git config --list`
- **Purpose:** Displays all current Git configuration settings.
- **Syntax:** `git config --list`
- **Example:**
```bash
git config --list
```

---

### `git config --unset`
- **Purpose:** Removes a specific configuration setting.
- **Syntax:** `git config --global --unset <key>`
- **Example:**
```bash
git config --global --unset user.name
```

---

## 2. Repository Setup Commands

### `git init`
- **Purpose:** Initializes a new empty Git repository in the current folder.
- **Syntax:** `git init`
- **Example:**
```bash
mkdir my-project && cd my-project
git init
```

---

### `git clone`
- **Purpose:** Copies a remote repository to your local machine.
- **Syntax:** `git clone <repository-url>`
- **Example:**
```bash
git clone https://github.com/username/repo.git
```

---

### `git clone --branch`
- **Purpose:** Clones a specific branch from a remote repository.
- **Syntax:** `git clone --branch <branch-name> <repository-url>`
- **Example:**
```bash
git clone --branch develop https://github.com/username/repo.git
```

---

### `git clone --depth`
- **Purpose:** Creates a shallow clone with limited commit history (faster).
- **Syntax:** `git clone --depth <number> <repository-url>`
- **Example:**
```bash
git clone --depth 1 https://github.com/username/repo.git
```

---

## 3. Repository Status & Inspection

### `git status`
- **Purpose:** Shows the working directory and staging area status.
- **Syntax:** `git status`
- **Example:**
```bash
git status
```

---

### `git log`
- **Purpose:** Shows the full commit history.
- **Syntax:** `git log`
- **Example:**
```bash
git log
```

---

### `git log --oneline`
- **Purpose:** Shows a compact one-line summary of each commit.
- **Syntax:** `git log --oneline`
- **Example:**
```bash
git log --oneline
```

---

### `git log --graph`
- **Purpose:** Displays commit history as a visual branch graph.
- **Syntax:** `git log --graph --oneline --all`
- **Example:**
```bash
git log --graph --oneline --all
```

---

### `git show`
- **Purpose:** Shows details of a specific commit or object.
- **Syntax:** `git show <commit-hash>`
- **Example:**
```bash
git show a1b2c3d
```

---

### `git diff`
- **Purpose:** Shows unstaged changes between working directory and last commit.
- **Syntax:** `git diff`
- **Example:**
```bash
git diff
```

---

### `git diff --staged`
- **Purpose:** Shows changes that are staged (ready to commit).
- **Syntax:** `git diff --staged`
- **Example:**
```bash
git diff --staged
```

---

### `git blame`
- **Purpose:** Shows who last modified each line of a file.
- **Syntax:** `git blame <filename>`
- **Example:**
```bash
git blame index.html
```

---

### `git reflog`
- **Purpose:** Shows a log of all local HEAD movements (useful for recovery).
- **Syntax:** `git reflog`
- **Example:**
```bash
git reflog
```

---

### `git shortlog`
- **Purpose:** Summarizes commit history grouped by author.
- **Syntax:** `git shortlog`
- **Example:**
```bash
git shortlog -sn
```

---

## 4. File Tracking Commands

### `git add`
- **Purpose:** Stages a specific file for commit.
- **Syntax:** `git add <filename>`
- **Example:**
```bash
git add index.html
```

---

### `git add .`
- **Purpose:** Stages all changed files in the current directory.
- **Syntax:** `git add .`
- **Example:**
```bash
git add .
```

---

### `git add -p`
- **Purpose:** Interactively stages specific chunks/parts of a file.
- **Syntax:** `git add -p`
- **Example:**
```bash
git add -p
```

---

### `git restore`
- **Purpose:** Discards changes in the working directory.
- **Syntax:** `git restore <filename>`
- **Example:**
```bash
git restore index.html
```

---

### `git restore --staged`
- **Purpose:** Unstages a file without discarding changes.
- **Syntax:** `git restore --staged <filename>`
- **Example:**
```bash
git restore --staged index.html
```

---

### `git rm`
- **Purpose:** Removes a file from the working directory and staging area.
- **Syntax:** `git rm <filename>`
- **Example:**
```bash
git rm old-file.txt
```

---

### `git mv`
- **Purpose:** Renames or moves a file and stages the change.
- **Syntax:** `git mv <old-name> <new-name>`
- **Example:**
```bash
git mv old-name.txt new-name.txt
```

---

## 5. Commit Commands

### `git commit`
- **Purpose:** Opens editor to write and save a commit message.
- **Syntax:** `git commit`
- **Example:**
```bash
git commit
```

---

### `git commit -m`
- **Purpose:** Commits staged changes with an inline message.
- **Syntax:** `git commit -m "message"`
- **Example:**
```bash
git commit -m "Added homepage layout"
```

---

### `git commit --amend`
- **Purpose:** Modifies the most recent commit (message or content).
- **Syntax:** `git commit --amend`
- **Example:**
```bash
git commit --amend -m "Fixed typo in commit message"
```

---

### `git commit --no-edit`
- **Purpose:** Amends the last commit without changing the commit message.
- **Syntax:** `git commit --amend --no-edit`
- **Example:**
```bash
git add forgotten-file.txt
git commit --amend --no-edit
```

---

## 6. Branch Management Commands

### `git branch`
- **Purpose:** Lists all local branches.
- **Syntax:** `git branch`
- **Example:**
```bash
git branch
```

---

### `git branch -a`
- **Purpose:** Lists all local and remote branches.
- **Syntax:** `git branch -a`
- **Example:**
```bash
git branch -a
```

---

### `git branch -d`
- **Purpose:** Deletes a branch (only if fully merged).
- **Syntax:** `git branch -d <branch-name>`
- **Example:**
```bash
git branch -d feature/login
```

---

### `git branch -D`
- **Purpose:** Force-deletes a branch regardless of merge status.
- **Syntax:** `git branch -D <branch-name>`
- **Example:**
```bash
git branch -D feature/login
```

---

### `git checkout`
- **Purpose:** Switches to an existing branch.
- **Syntax:** `git checkout <branch-name>`
- **Example:**
```bash
git checkout main
```

---

### `git checkout -b`
- **Purpose:** Creates and switches to a new branch.
- **Syntax:** `git checkout -b <new-branch>`
- **Example:**
```bash
git checkout -b feature/signup
```

---

### `git switch`
- **Purpose:** Modern way to switch branches.
- **Syntax:** `git switch <branch-name>`
- **Example:**
```bash
git switch develop
```

---

### `git switch -c`
- **Purpose:** Creates and switches to a new branch (modern syntax).
- **Syntax:** `git switch -c <new-branch>`
- **Example:**
```bash
git switch -c feature/dashboard
```

---

## 7. Merge & Integration Commands

### `git merge`
- **Purpose:** Merges another branch into the current branch.
- **Syntax:** `git merge <branch-name>`
- **Example:**
```bash
git merge feature/signup
```

---

### `git merge --no-ff`
- **Purpose:** Merges with a merge commit even if fast-forward is possible.
- **Syntax:** `git merge --no-ff <branch-name>`
- **Example:**
```bash
git merge --no-ff feature/signup
```

---

## 8. Remote Repository Commands

### `git remote`
- **Purpose:** Lists configured remote connections.
- **Syntax:** `git remote`
- **Example:**
```bash
git remote
```

---

### `git remote -v`
- **Purpose:** Shows remote URLs (fetch and push).
- **Syntax:** `git remote -v`
- **Example:**
```bash
git remote -v
```

---

### `git remote add`
- **Purpose:** Adds a new remote connection.
- **Syntax:** `git remote add <name> <url>`
- **Example:**
```bash
git remote add origin https://github.com/username/repo.git
```

---

### `git remote remove`
- **Purpose:** Removes a remote connection.
- **Syntax:** `git remote remove <name>`
- **Example:**
```bash
git remote remove origin
```

---

### `git fetch`
- **Purpose:** Downloads changes from remote without merging.
- **Syntax:** `git fetch <remote>`
- **Example:**
```bash
git fetch origin
```

---

### `git fetch --all`
- **Purpose:** Fetches from all configured remotes.
- **Syntax:** `git fetch --all`
- **Example:**
```bash
git fetch --all
```

---

### `git pull`
- **Purpose:** Fetches and merges changes from remote.
- **Syntax:** `git pull <remote> <branch>`
- **Example:**
```bash
git pull origin main
```

---

### `git pull --rebase`
- **Purpose:** Fetches and rebases instead of merging.
- **Syntax:** `git pull --rebase`
- **Example:**
```bash
git pull --rebase origin main
```

---

### `git push`
- **Purpose:** Uploads local commits to the remote repository.
- **Syntax:** `git push <remote> <branch>`
- **Example:**
```bash
git push origin main
```

---

### `git push -u origin branch-name`
- **Purpose:** Pushes and sets upstream tracking for the branch.
- **Syntax:** `git push -u origin <branch-name>`
- **Example:**
```bash
git push -u origin feature/login
```

---

### `git push --force`
- **Purpose:** Force-pushes local commits, overwriting remote history (use with caution).
- **Syntax:** `git push --force`
- **Example:**
```bash
git push --force origin feature/login
```

---

## 9. Stash Commands

### `git stash`
- **Purpose:** Temporarily saves uncommitted changes.
- **Syntax:** `git stash`
- **Example:**
```bash
git stash
```

---

### `git stash list`
- **Purpose:** Lists all saved stashes.
- **Syntax:** `git stash list`
- **Example:**
```bash
git stash list
```

---

### `git stash pop`
- **Purpose:** Applies the latest stash and removes it from the stash list.
- **Syntax:** `git stash pop`
- **Example:**
```bash
git stash pop
```

---

### `git stash apply`
- **Purpose:** Applies a stash without removing it from the list.
- **Syntax:** `git stash apply stash@{0}`
- **Example:**
```bash
git stash apply stash@{0}
```

---

### `git stash drop`
- **Purpose:** Deletes a specific stash entry.
- **Syntax:** `git stash drop stash@{0}`
- **Example:**
```bash
git stash drop stash@{0}
```

---

### `git stash clear`
- **Purpose:** Removes all stashed entries.
- **Syntax:** `git stash clear`
- **Example:**
```bash
git stash clear
```

---

## 10. Reset & Undo Commands

### `git reset`
- **Purpose:** Resets the staging area to match a commit.
- **Syntax:** `git reset <commit>`
- **Example:**
```bash
git reset HEAD~1
```

---

### `git reset --soft`
- **Purpose:** Moves HEAD back but keeps changes staged.
- **Syntax:** `git reset --soft <commit>`
- **Example:**
```bash
git reset --soft HEAD~1
```

---

### `git reset --mixed`
- **Purpose:** Moves HEAD back and unstages changes (default behavior).
- **Syntax:** `git reset --mixed <commit>`
- **Example:**
```bash
git reset --mixed HEAD~1
```

---

### `git reset --hard`
- **Purpose:** Moves HEAD back and discards all changes permanently.
- **Syntax:** `git reset --hard <commit>`
- **Example:**
```bash
git reset --hard HEAD~1
```

---

### `git revert`
- **Purpose:** Creates a new commit that undoes a previous commit safely.
- **Syntax:** `git revert <commit-hash>`
- **Example:**
```bash
git revert a1b2c3d
```

---

### `git clean -f`
- **Purpose:** Removes untracked files from the working directory.
- **Syntax:** `git clean -f`
- **Example:**
```bash
git clean -f
```

---

### `git clean -fd`
- **Purpose:** Removes untracked files and directories.
- **Syntax:** `git clean -fd`
- **Example:**
```bash
git clean -fd
```

---

## 11. Rebasing Commands

### `git rebase`
- **Purpose:** Moves or replays commits on top of another branch.
- **Syntax:** `git rebase <branch>`
- **Example:**
```bash
git rebase main
```

---

### `git rebase -i`
- **Purpose:** Interactively rebase to edit, squash, or reorder commits.
- **Syntax:** `git rebase -i HEAD~<n>`
- **Example:**
```bash
git rebase -i HEAD~3
```

---

### `git rebase --continue`
- **Purpose:** Continues rebase after resolving conflicts.
- **Syntax:** `git rebase --continue`
- **Example:**
```bash
git rebase --continue
```

---

### `git rebase --abort`
- **Purpose:** Cancels an in-progress rebase and restores original state.
- **Syntax:** `git rebase --abort`
- **Example:**
```bash
git rebase --abort
```

---

## 12. Cherry Pick & Patch Commands

### `git cherry-pick`
- **Purpose:** Applies a specific commit from another branch to the current branch.
- **Syntax:** `git cherry-pick <commit-hash>`
- **Example:**
```bash
git cherry-pick a1b2c3d
```

---

### `git format-patch`
- **Purpose:** Creates patch files from commits to share via email or file.
- **Syntax:** `git format-patch HEAD~<n>`
- **Example:**
```bash
git format-patch HEAD~2
```

---

### `git apply`
- **Purpose:** Applies a patch file to the working directory.
- **Syntax:** `git apply <patch-file>`
- **Example:**
```bash
git apply 0001-fix-bug.patch
```

---

### `git am`
- **Purpose:** Applies a patch file as a commit (with commit metadata).
- **Syntax:** `git am <patch-file>`
- **Example:**
```bash
git am 0001-fix-bug.patch
```

---

## 13. Tagging Commands

### `git tag`
- **Purpose:** Lists all tags or creates a lightweight tag.
- **Syntax:** `git tag` or `git tag <tag-name>`
- **Example:**
```bash
git tag v1.0
```

---

### `git tag -a`
- **Purpose:** Creates an annotated tag with a message.
- **Syntax:** `git tag -a <tag-name> -m "message"`
- **Example:**
```bash
git tag -a v1.0 -m "First stable release"
```

---

### `git tag -d`
- **Purpose:** Deletes a local tag.
- **Syntax:** `git tag -d <tag-name>`
- **Example:**
```bash
git tag -d v1.0
```

---

### `git push origin --tags`
- **Purpose:** Pushes all local tags to the remote repository.
- **Syntax:** `git push origin --tags`
- **Example:**
```bash
git push origin --tags
```

---

## 14. Submodule Commands

### `git submodule add`
- **Purpose:** Adds another Git repository as a submodule inside this repo.
- **Syntax:** `git submodule add <url> <path>`
- **Example:**
```bash
git submodule add https://github.com/username/lib.git libs/mylib
```

---

### `git submodule init`
- **Purpose:** Initializes submodule configuration after cloning.
- **Syntax:** `git submodule init`
- **Example:**
```bash
git submodule init
```

---

### `git submodule update`
- **Purpose:** Fetches and checks out submodule content.
- **Syntax:** `git submodule update`
- **Example:**
```bash
git submodule update --init --recursive
```

---

## 15. Debugging Commands

### `git bisect`
- **Purpose:** Uses binary search to find the commit that introduced a bug.
- **Syntax:** `git bisect start`
- **Example:**
```bash
git bisect start
```

---

### `git bisect start`
- **Purpose:** Starts the bisect session.
- **Syntax:** `git bisect start`
- **Example:**
```bash
git bisect start
```

---

### `git bisect good`
- **Purpose:** Marks a commit as good (bug not present).
- **Syntax:** `git bisect good <commit>`
- **Example:**
```bash
git bisect good v1.0
```

---

### `git bisect bad`
- **Purpose:** Marks a commit as bad (bug is present).
- **Syntax:** `git bisect bad`
- **Example:**
```bash
git bisect bad HEAD
```

---

## GitHub Features Demonstrated

| Feature | Description |
|---|---|
| Create Repository | Created a new public repository on GitHub |
| Add README | Added README.md describing the project |
| Add .gitignore | Added .gitignore to exclude unnecessary files |
| Create Issue | Opened an issue to track a task |
| Assign Issue | Assigned the issue to a team member |
| Create Branch | Created a feature branch from main |
| Push Branch | Pushed the branch to GitHub |
| Create Pull Request | Opened a PR to merge feature branch |
| Review Pull Request | Added comments and approved the PR |
| Merge Pull Request | Merged the PR into main |
| Resolve Merge Conflict | Fixed conflicts between branches |
| Close Issue | Closed the issue after completion |
| Add Labels | Applied labels like `bug`, `enhancement` |
| Add Collaborators | Invited collaborators to the repository |

---

*Submitted by: [Your Name] | Repository contains screenshot proof for each command.*
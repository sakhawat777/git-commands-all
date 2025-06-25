Git Commands
============

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git commit --amend` | This will update the previous commit with the currently staged changes |
| `git rm -r [folder-name]` | Remove a folder (or file) |
| `git rm [file-name.txt]` | Remove a file |
| `git rm -r --cached [folder-name]` | To stop tracking a folder in Git but keep it locally|
| `git rm --cached [file-name.txt]` | To stop tracking a file in Git but keep it locally |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git switch -c <new-branch-name>` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git switch [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git merge --abort` | Aborts the current merge process and resets the working directory to the state before the merge started |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git rebase main` | Re-applies your current branch’s commits on top of the latest main branch — for a cleaner, linear history |
| `git rebase --abort` | Abort a rebase (if conflicts go wrong) |
| `git rebase --continue` | Resumes the rebase process after resolving conflicts from a previous commit during rebase |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git push origin -f` | Forcefully pushes the local branch to the remote origin, overwriting its history |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote -v` |  Lists all remote repositories with their fetch/push URLs |
| `git remote show origin` | Displays info like fetch/push URLs, branches tracked, and more |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
 `git remote add admin ssh://git@github.com/[username]/[repository-name].git` | Adds a new remote repository named admin |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git remote remove origin` | Removes the remote named origin from your Git repository configuration |
| `git remote set-url --delete origin git@github.com/user/repo1.git` | Remove one specific URL |
| `git remote rename origin upstream` | Renames remote origin to upstream |
| `git fetch origin` | Downloads commits, branches, and tags from origin without merging |
| `git fetch origin main` | Fetch latest from remote main |
| `git fetch --all` | Fetch all remotes |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |

### Shows Differences between Commits, Branches, or Working Directory vs Staged

| Command | Description |
| ------- | ----------- |
| `git diff` | Unstaged changes |
| `git diff --staged` | Staged changes |
| `git diff main feature` | Differences between branches |


### Undo Local Changes, Reset History, and Clean Working Directory

| Command | Description |
| ------- | ----------- |
| `git restore --staged file.txt` | Unstage |
| `git restore --staged <file1> <file2> ...` | unstages one or more files that were previously added to the staging area |
| `git restore file.txt` | Discard working changes |
| `git reset --soft cd4456` | Moves HEAD to commit cd4456, keeping all changes from newer commits staged |
| `git reset --soft HEAD~1` | Moves HEAD to the previous commit and keeps all changes staged for a new commit (affect local) |
| `git reset --soft HEAD~3` | Moves HEAD back by 3 commits, keeping all changes staged for recommit (affect local) |
| `git reset --hard HEAD~1` | Moves HEAD back one commit, deletes changes permanently from staging and working directory unless recovered via git reflog (affect local) |
| `git reset --hard HEAD~3` | Completely deletes the last 3 commits and discards all related changes from working directory and staging area (affect local) |
| `git push origin your-branch --force` | Forcefully pushes your local branch to the remote, overwriting remote history and potentially overwriting others’ work |
| `git push origin -f` | Forcibly pushes the current branch to origin, overwriting remote changes |
| `git clean -f` | Removes untracked files from your working directory |


### Git Cherry-Pick Commands

| Command | Description |
| ------- | ----------- |
| `git cherry-pick <commit-hash>` | Applies the given commit to the current branch |
| `git cherry-pick <commit1> <commit2> ...` | Applies multiple commits in order to your current branch |
| `git cherry-pick <start-commit>^..<end-commit>` | Applies a continuous sequence of commits from start-commit (inclusive) to end-commit |
| `git cherry-pick --abort | Cancels the cherry-pick if a conflict occurs, restoring the branch to its previous state |
| `git cherry-pick --continue` | After resolving conflicts, this finalizes the cherry-pick |
| `git cherry-pick --skip` | Skips the commit if you don’t want to apply it due to conflict or irrelevance |

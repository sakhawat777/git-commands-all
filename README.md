Complete Git Commands Solutions: Author: Md. Sakhawat Hossain
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
| `git add .` | Adds all changed (new or modified) files in the current directory and subdirectories to the staging area |
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
| `git checkout <commit-hash>` | View specific commit in detached HEAD mode |
| `git checkout -b bugfix 4f3d2a1` | Creates and switches to branch bugfix starting from commit 4f3d2a1 |
| `git switch [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git merge --abort` | Aborts the current merge process and resets the working directory to the state before the merge started |
| `git stash` | Stash changes in a dirty working directory |
| `git stash apply` | Applies the most recent stash without deleting it |
| `git stash list` | Lists all stashed changes |
| `git stash drop` | Deletes a specific stash |
| `git stash pop` | Applies the latest stash and removes it from the stash list |
| `git stash branch <branchname>` | Creates a branch from a stash and applies it |
| `git stash clear` | Remove all stashed entries |
| `git rebase main` | Re-applies your current branch’s commits on top of the latest main branch — for a cleaner, linear history |
| `git rebase --abort` | Abort a rebase (if conflicts go wrong) |
| `git rebase --continue` | Resumes the rebase process after resolving conflicts from a previous commit during rebase |
| `git rebase -i HEAD~3` |  Interactively edit, reorder, squash the last 3 commits |

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
| `git remote add upstream https://github.com/original-user/original-repo.git` | Adds the original repository as a remote called upstream to your local repository |
| `git fetch upstream` | Downloads the latest changes from the upstream repository, including all branches |
| `git checkout upstream/main` | Switches your local working directory to the upstream branch. Note that you cannot directly commit to this branch |
| `git push --set-upstream origin <your-branch-name>>` | Here, -u is the shorthand for --set-upstream, which links your local branch with the remote branch |
| `git branch -vv` | Shows upstream tracking per branch |
| `git fetch origin` | Downloads commits, branches, and tags from origin without merging |
| `git remote rename origin upstream` | Renames remote origin to upstream |
| `git remote remove upstream` | Removes the upstream remote link from your local Git configuration |
| `git fetch origin main` | Fetch latest from remote main |
| `git fetch --all` | Fetch all remotes |
| `git fetch --prune` | Remove remote-tracking references that no longer exist on remote |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
| `git log --graph --oneline --decorate --all` | Pretty graph of commit history |

### Shows Differences between Commits, Branches, or Working Directory vs Staged

| Command | Description |
| ------- | ----------- |
| `git diff` | Unstaged changes |
| `git diff --staged` | Staged changes |
| `git diff main feature` | Differences between branches |
| `git diff --name-only` | Show only filenames that changed |
| `git diff --stat` |  Show summary stats of changes |
| `git diff <commit1> <commit2> -- <file>` | Diff for a specific file between commits |

### Undo Local Changes, Reset History, and Clean Working Directory

| Command | Description |
| ------- | ----------- |
| `git restore --staged file.txt` | Unstage |
| `git restore --staged <file1> <file2> ...` | unstages one or more files that were previously added to the staging area |
| `git restore file.txt` | Discard working changes |
| `git reset --soft cd4456` | Moves HEAD to commit cd4456, keeping all changes from newer commits staged |
| `git reset --soft HEAD~` | Moves HEAD to the previous commit and keeps all changes staged for a new commit (affect local) |
| `git reset --soft HEAD~1` | Moves HEAD to the previous commit and keeps all changes staged for a new commit (affect local) |
| `git reset --soft HEAD~3` | Moves HEAD back by 3 commits, keeping all changes staged for recommit (affect local) |
| `git reset --hard HEAD~` | Moves HEAD back one commit, deletes changes permanently from staging and working directory unless recovered via git reflog (affect local) |
| `git reset --hard HEAD~1` | Moves HEAD back one commit, deletes changes permanently from staging and working directory unless recovered via git reflog (affect local) |
| `git reset --hard HEAD~3` | Completely deletes the last 3 commits and discards all related changes from working directory and staging area (affect local) |
| `git push origin your-branch --force` | Forcefully pushes your local branch to the remote, overwriting remote history and potentially overwriting others’ work |
| `git push origin -f` | Forcibly pushes the current branch to origin, overwriting remote changes |
| `git clean -f folder/` | Delete untracked files in the folder |
| `git clean -f` | Removes untracked files from your working directory |
| `git clean -fd` | Permanently removes all untracked files and directories from your working directory |
| `git clean -fdn` | This will show you what will be deleted without actually deleting it |
| `git clean -fx` | Forcefully removes all untracked files, including files ignored by .gitignore, from your working directory |


### Git Config Commands

| Command | Description |
| ------- | ----------- |
| `git config --list` | List current config |
| `git config user.name "Your Name"` | Set username locally |
| `git config user.email "email@example.com"` | Set email locally |


### Git Blame Commands

| Command | Description |
| ------- | ----------- |
| `git blame <file>` | Shows line-by-line author info for a file |


### Git Archive With Prefix Commands

| Command | Description |
| ------- | ----------- |
| `git archive --prefix=project-v1/ -o project-v1.zip v1.0.0` | Create archive with folder prefix |



### Tag Commands

| Command | Description |
| ------- | ----------- |
| `git tag`| Shows all tags in the repository |
| `git tag v1.0.0` | Creates a tag named v1.0.0 on the current HEAD commit |
| `git tag -a v1.0.0 -m "Release version 1.0.0` |  Creates a tag with metadata like tagger name, date, and a message. Recommended for releases |
| `git tag -a v1.0.0 abc1234 -m "Tagging old commit"` | Tags commit abc1234 with v1.0.0 |
| `git show v1.0.0` | Displays info about the tag and the commit it points to |
| `git push origin v1.0.0` | Uploads only v1.0.0 tag to the remote repo |
| `git push origin --tags` | Pushes all local tags to the remote repository |
| `git tag -d v1.0.0` | Deletes the tag from your local repository |
| `git push origin --delete tag v1.0.0` | Deletes the tag from the remote repository |
| `git checkout v1.0.0` | Checks out the tagged version in detached HEAD mode. You’re not on a branch |
| `git checkout -b hotfix v1.0.0` | Creates and switches to a new branch hotfix from the v1.0.0 tag |
| `git archive --format=zip --output=v1.0.0.zip v1.0.0` | Creates a zip of the code as it was at the tagged version |


### Git Cherry-Pick Commands

| Command | Description |
| ------- | ----------- |
| `git cherry-pick <commit-hash>` | Applies the given commit to the current branch |
| `git cherry-pick <commit1> <commit2> ...` | Applies multiple commits in order to your current branch |
| `git cherry-pick <start-commit>^..<end-commit>` | Applies a continuous sequence of commits from start-commit (inclusive) to end-commit |
| `git cherry-pick --abort` | Cancels the cherry-pick if a conflict occurs, restoring the branch to its previous state |
| `git cherry-pick --continue` | After resolving conflicts, this finalizes the cherry-pick |
| `git cherry-pick --skip` | Skips the commit if you don’t want to apply it due to conflict or irrelevance |
| `git cherry-pick -e <commit-hash>` | Lets you edit the commit message during the cherry-pick |
| `git cherry-pick -n <commit-hash>` | Applies the changes from the commit but leaves them staged (not committed) |


### Reflog & Recovery

| Command | Description |
| ------- | ----------- |
| `git reflog` | Shows a log of all changes to HEAD (great for recovering lost commits) |
| `git reset HEAD@{1}` | Reset to the previous state using reflog |

### Essential Git Commands for Managing Local Changes and Ignoring Files

| Command | Description |
| ------- | ----------- |
| `git update-index --assume-unchanged .gitlab-ci.yml deploy.log` | Temporarily ignore any changes made to .gitlab-ci.yml and deploy.log in your local working directory |
| `git update-index --no-assume-unchanged <file>` | Undo the effect of --assume-unchanged, so Git tracks changes again |
| `git ls-files -v` | Lists all Git-tracked files with a prefix showing their status — e.g., h for files marked as --assume-unchanged, M for modified, and space for clean. |
| `echo "file.txt" >> .gitignore` | Appends file.txt to .gitignore to tell Git to ignore this file in future commits |



### General Rollback Steps
| Command | Description |
| ------- | ----------- |
| 1st Way | Best for Shared/Remote Branches |
| `git log --oneline` | Check your commit history|
| `git revert <commit-hash>` | git revert <commit> — Best for Shared/Remote Branches |
| `git push origin main` | Rolling back changes on branches others are using (e.g., main, develop) |
| 2nd Way | Rollback but keep changes staged (soft reset) |
| `git log --oneline` | Check your commit history|
| `git reset --soft <commit-hash>` | Rollback but keep changes staged (soft reset) |
| `git push origin <branch-name> --force` | If you already pushed the commits and want to update the remote branch (force push needed) |
| 3rd Way | Best for Solo Projects / Local Rollback |
| `git log --oneline` | Check your commit history|
| `git reset --hard <commit>` | Best for Solo Projects / Local Rollback |
| `git push origin <branch-name> --force` | If you already pushed the commits and want to update the remote branch (force push needed) |
| 4th Way | Best for Rewriting Commits |
| `git log --oneline` | Check your commit history|
| `git reset --soft HEAD~1` | Best for Rewriting Commits |
| `git commit -m "Better commit message` | Rewording or squashing recent commits before pushing |
| `git push origin <branch-name> --force` | If you already pushed the commits and want to update the remote branch (force push needed) |
| 5th Way | Rollback and keep changes unstaged (mixed reset, default) |
| `git log --oneline` | Check your commit history|
| `git reset --mixed <commit-hash>` | Undo commits and keep changes in your working directory but unstaged |
| `git add .` | Adds **all modified and new files** in the current directory (and subdirectories) to the staging area |
| `git commit -m "Revised commit after rollback"` | Create a new commit |
| `git push origin <branch-name> --force` | If you already pushed the commits and want to update the remote branch (force push needed) |


| Golden Rule: | Use revert on shared/public branches. Use reset only when you understand the risks and coordinate with your team |

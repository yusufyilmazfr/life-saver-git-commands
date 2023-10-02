# Life and Time Saver Git Commands 🚀
A repository that contains life and timer saver git commands; rollback, revert, etc. (in-progress)

- [How to delete all local git branches?](#how-to-delete-all-local-git-branches)
- [How to undo the last commit from a remote git repository?](#how-to-undo-the-last-commit-from-a-remote-git-repository)
- [How to revert merge?](#how-to-revert-merge)
- [How to revert conflicted merge?](#how-to-revert-conflicted-merge)

<hr/>

#### How to delete all local git branches?
```bash
git branch --list | grep -v 'master' | xargs git branch -D
```

#### How to undo the last commit from a remote git repository?
```bash
git reset HEAD^
git push origin +HEAD
```

#### How to revert merge?
```bash
# create new branch for being safe.
git revert -m 1 <MERGE_COMMIT_ID>
git push
```

#### How to revert conflicted merge?
```bash
git merge --abort
```

### How do you add a message to stash?
```bash
git stash save "Your stash message"
```
###How do you retrieve recordings from Stash?
```bash
git stash list
```

### How do you bring any record from the Stash list without removing it from the list?
 ```bash
 git stash apply 
 ```
  from history n. applies stashed recording
 ```bash
 git stash apply stash@{n}
 # shortcut
 git stash apply {n}
 ```

### How do you bring the last entry to the Stash list and remove it from the list?
 ```bash
 git stash pop 
 ```

### How do I delete a record from the Stash list?
 ```bash
 git stash drop 
 ```

### How do I move the latest changes I added to Stash to a different branch?
 ```bash
 git stash branch new-branch-name
 ```


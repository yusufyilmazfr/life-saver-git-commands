# Life and Time Saver Git Commands 🚀
A repository that contains life and timer saver git commands; rollback, revert, etc. (in-progress)

- [How to delete all local git branches?](#how-to-delete-all-local-git-branches)
- [How to undo the last commit from a remote git repository?](#how-to-undo-the-last-commit-from-a-remote-git-repository)
- [How to revert merge?](#how-to-revert-merge)
- [How to revert conflicted merge?](#how-to-revert-conflicted-merge)
- [How do you bring any record from the Stash list without removing it from the list?](#how-do-you-bring-any-record-from-the-stash-list-without-removing-it-from-the-list)


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

#### How to add a message to stash?
```bash
git stash save "Your stash message"
```

#### How to list stash?
```bash
git stash list
```

#### How to bring nth record from the stash list without removing it?
 ```bash
 git stash apply {n} # n is optional, from nth history.
 ```

#### How to bring last entry to the stash list and remove?
 ```bash
 git stash pop 
 ```

#### How to delete a stash record from the list?
 ```bash
 git stash drop 
 ```

#### How to move latest changes to stash with different branch?
 ```bash
 git stash branch <new-branch-name>
 ```


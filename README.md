# Life and Time Saver Git Commands 🚀
A repository that contains life and timer saver git commands; rollback, revert, etc. (in-progress)

- [How to delete all local git branches?](#how-to-delete-all-local-git-branches)
- [How to undo the last commit from a remote git repository?](#how-to-undo-the-last-commit-from-a-remote-git-repository)

<hr/>

### How to delete all local git branches?
```bash
git branch --list | grep -v 'master' | xargs git branch -D
```

#### How to undo the last commit from a remote git repository?
```bash
git reset HEAD^
git push origin +HEAD
```

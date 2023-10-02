# Life and Time Saver Git Commands 🚀
A repository that contains life and timer saver git commands; rollback, revert, etc. (in-progress)

- [How to delete all local git branches?](#how-to-delete-all-local-git-branches)
- [How to undo the last commit from a remote git repository?](#how-to-undo-the-last-commit-from-a-remote-git-repository)

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

#### How to undo the last commit from a remote git repository?
```bash
git reset HEAD^
git push origin +HEAD
```


# Stash

## What is Git Stash?

Git Stash temporarily saves changes in your working directory without committing them to a branch. This can be useful when switching to a different branch or working on another task without committing your current changes.

## Git Stash Commands

### `git stash save`

- **Description**: This command is used to save your current changes in the stash.
- **Usage**:
   ```shell
   git stash save "Your stash message"

### `git stash list`

- **Description**: This command lists all the stashes you've created.
- **Usage**:
   ```shell
   git stash list

### `git stash apply`

- **Description**: This command applies the most recent stash to your working directory. But it doesn't delete it from the stash list
- **Usage**:
   ```shell
   git stash apply 
   ```
    from history n. applies stashed recording
   ```shell
   git stash apply stash@{n}
   # shortcut
   git stash apply {n}
   ```

### `git stash pop`

- **Description**: This command applies the most recent stash and removes it from the stash list.
- **Usage**:
   ```shell
   git stash pop 
   ```
    from history n. applies stashed recording
   ```shell
   git stash pop stash@{n}
   # shortcut
   git stash pop {n}
   ```
   
### `git stash drop`

- **Description**: This command deletes a specific stash from the stash list.
- **Usage**:
   ```shell
    git stash drop stash@{n}

### `git stash branch`

- **Description**: This command creates a new branch and applies the most recent stash to it.
- **Usage**:
   ```shell
    git stash branch new-branch-name

### `git stash clear`

- **Description**: This command removes all stashes
- **Usage**:
   ```shell
    git stash clear


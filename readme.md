# Gitting around
This project is about familiarizing yourself with git. It involves moving around in a repository with multiple branches (you do not need to create these) to solve different tasks. Solving these tasks may give confidence in your knowledge of git repository structure and of using the more advanced features for profit.

To be able to solve the exercises you first need to learn how to list branches and how to switch to them as the exercises for the tasks can be found on separate branches.

## Tasks

### Initialize exercises
Initialize your repository by running the initialization script, bash ./helper/init. This will create branches needed for the following tasks.
1. Executing the git branch command in shell returns the following output.
```bash
collect-files
find-secret
* development
remote-change
resolve-conflict
size-history
```

### Merge remote change
Switch to the remote-change branch and pull the changes from the remote.

1. After executing git checkout remote-change, executing git log shows a new merge commit starting with: "Merge branch 'remote-change' ..." on the top of the output.

2. After executing git checkout remote-change executing git status shows the following output.
```bash
On branch remote-change
Your branch is ahead of 'origin/remote-change' by 2 commits.
(use "git push" to publish your local commits)

nothing to commit, working tree clean
```

### Resolve conflict
Switch to the resolve-conflict branch, pull the changes from the remote and resolve conflicts.

1. After executing git checkout resolve-conflict, the contents of work.txt should look like:
```bash
I work
I rest after I work
```

2. After executing git checkout resolve-conflict the git log shows a new merge commit starting with the following line. "Merge branch 'resolve-conflict' ..."

### Find a secret
Find the secret about the meaning of 42 by investigating the git history of the find-secret branch. Experiment with some git commands to see what has changed in the previous commits.

1. Knowledge of what 42 means in programming.

### Collect size changes of a file
On the size-history branch there are multiple commits changing the names.txt file. Find all versions of names.txt and the size (in bytes) for each version. Collect all sizes of names.txt separated by commas in a new result.txt file starting with the oldest, then commit your changes. You should visit all previous commits of this repository and observe the size of a changing file.

1. Executing git log --name-only after executing git checkout size-history shows a new commit adding result.txt.

2. The commit message is meaningful and describes the change accurately.

3. Executing cat result.txt after executing git checkout size-history in the shell shows a 5 elements list starting with 35, ending with 89

### Collect all files that ever existed
On the collect-files branch there were several files created, some still exist. Find the names of all files that ever existed on the branch, collect all the names separated by commas in a new result.txt file, then commit your changes. You should visit all previous commits of this repository and observe which files exist.

1. After executing git checkout collect-files, the last commit message is meaningful and describes the change accurately.

2. Executing git log --name-only after executing git checkout collect-files shows a new commit adding result.txt.

3. Executing cat result.txt after executing git checkout collect-files in the shell shows 14 (or 16 if . and .. are included) lines.

## Hints
* Always make sure that you are on the correct branch when working on an exercise.
* Use git log --oneline for a succinct view of the history of the current branch.
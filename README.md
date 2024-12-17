# GIT Exercise

## Bundle 1

### Exercise 1

```bash
gymumuco@umucos-iMac-2 dec2024 % mkdir gitExercise1-B1
gymumuco@umucos-iMac-2 dec2024 % cd gitExercise1-B1 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git init
Initialized empty Git repository in /Users/gymumuco/Documents/theGYMVARMA/dec2024/gitExercise1-B1/.git/
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch README.md
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status  
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git branch -m master
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git branch -m main
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "change branch name from master to main. create readme file" 
[main (root-commit) 22b77ec] change branch name from master to main. create readme file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
gymumuco@umucos-iMac-2 gitExercise1-B1 % git remote add origin git@github.com:varma-cephas/gitExercise1-B1.git
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 234 bytes | 234.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      main -> main
gymumuco@umucos-iMac-2 gitExercise1-B1 % git branch dev
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status
On branch main
nothing to commit, working tree clean
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout dev
Switched to branch 'dev'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git branch test
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout test
Switched to branch 'test'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout dev
Switched to branch 'dev'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git branch -d test
Deleted branch test (was 22b77ec).
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status
On branch dev
nothing to commit, working tree clean
```

### Exercise 2

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch home.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add home.html 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash
Saved working directory and index state WIP on dev: 22b77ec change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch about.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add about.html 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash
Saved working directory and index state WIP on dev: 22b77ec change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add team.html 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash
Saved working directory and index state WIP on dev: 22b77ec change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash list
stash@{0}: WIP on dev: 22b77ec change branch name from master to main. create readme file
stash@{1}: WIP on dev: 22b77ec change branch name from master to main. create readme file
stash@{2}: WIP on dev: 22b77ec change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html

Dropped stash@{1} (32df2ad28142e30dce0582b553bbe2ddd89bb052)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash list         
stash@{0}: WIP on dev: 22b77ec change branch name from master to main. create readme file
stash@{1}: WIP on dev: 22b77ec change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html
	new file:   home.html

Dropped stash@{1} (10a16f669e609b628667508eb75de7af1fe51454)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "added home and about html files`'
dquote bquote> 
dquote bquote> "
dquote bquote> ;
dquote bquote> 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "added home and about html files" 
[dev bbdeae5] added home and about html files
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Everything up-to-date
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin dev
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 502 bytes | 502.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercise1-B1/pull/new/dev
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git stash pop stash@{0}               
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   team.html

Dropped stash@{0} (d24c2a9d38566200d2c20ef8703d7451bb93c968)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   team.html

gymumuco@umucos-iMac-2 gitExercise1-B1 % git reset
```
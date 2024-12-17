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

## Bundle 2

### Exercise 1

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch services.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "made changes in home, about and services files"
[ft/bundle-2 770d37e] made changes in home, about and services files
 4 files changed, 27 insertions(+)
 create mode 100644 services.html
 create mode 100644 team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/bundle-2
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 736 bytes | 736.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExerciseOneTwo-B1.git
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExerciseOneTwo-B1/pull/new/ft/bundle-2
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```

### Exercise 2

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git pull origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 892 bytes | 892.00 KiB/s, done.
From github.com:varma-cephas/gitExercise1-B1
 * branch            main       -> FETCH_HEAD
   22b77ec..583a938  main       -> origin/main
Updating 22b77ec..583a938
Fast-forward
 about.html    | 15 +++++++++++++++
 home.html     | 12 ++++++++++++
 services.html | 11 +++++++++++
 team.html     | 11 +++++++++++
 4 files changed, 49 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html
 create mode 100644 team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our services page with more recent content"
[ft/service-redesign 6539137] updated our services page with more recent content
 1 file changed, 12 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/service-redesign
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 565 bytes | 565.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExerciseOneTwo-B1.git
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExerciseOneTwo-B1/pull/new/ft/service-redesign
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our services with the new stock products, we should be more profitable at this point"
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our services with the new stock products, we should be more profitable at this point"
[main 044e5de] updated our services with the new stock products, we should be more profitable at this point
 1 file changed, 12 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 644 bytes | 644.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExerciseOneTwo-B1.git
To github.com:varma-cephas/gitExercise1-B1.git
   583a938..044e5de  main -> main
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git diff main
diff --git a/services.html b/services.html
index 933b254..ce5b225 100644
--- a/services.html
+++ b/services.html
@@ -11,13 +11,13 @@
     <p>We're now back into business though</p>
     <h4>Our new product line-up includes:</h4>
     <ul>
-        <li>Something more</li>
-    </ul>
-    <p>Our product line need to to be changed, so we did exactly that.</p>
-    <ul>
-        <li>And more</li>
-        <li>And more</li>
-        <li>And more</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
+        <li>Nothing much</li>
     </ul>
 </body>
 </html>
\ No newline at end of file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge ft/service-redesign
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge --abort
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/service-redesign
services.html: needs merge
error: you need to resolve your current index first
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge --abort
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge main                  
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status    
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge main
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge main
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git status 
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
	modified:   services.html

gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit "resolved merge conflict on services file"
fatal: cannot do a partial commit during a merge.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "resolved merge conflict on services file"
[ft/service-redesign febc6fb] resolved merge conflict on services file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Everything up-to-date
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/service-redesign                
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 225 bytes | 225.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExerciseOneTwo-B1.git
To github.com:varma-cephas/gitExercise1-B1.git
   6539137..febc6fb  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```
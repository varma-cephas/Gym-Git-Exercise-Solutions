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

## Bundle 3

### Exercise 1

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "add team page and updated content"
[ft/team-page be59dc0] add team page and updated content
 1 file changed, 14 insertions(+)
 create mode 100644 team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/team-page
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 632 bytes | 632.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/team-page
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git log
commit be59dc041a34ec3b30c6603966bc7a2bc3254d27 (HEAD -> ft/team-page, origin/ft/team-page)
Author: varmac <varmac231@gmail.com>
Date:   Wed Dec 18 11:24:02 2024 +0200

    add team page and updated content

commit 15514a21cd3730a9383ba86cd380e39230278f80 (ft/service-redesign)
Merge: febc6fb 4b8164b
Author: varmac <varmac231@gmail.com>
Date:   Wed Dec 18 11:17:51 2024 +0200

    Merge branch 'main' of github.com:varma-cephas/gitExercise1-B1 into ft/service-redesign
    this branch is behind the main one, that's the reason the merge is necessay

commit 4b8164b895063e78255928fde2a6ccacdf526220 (origin/main, main, ft/contact-page)
Author: varmac <varmac231@gmail.com>
Date:   Wed Dec 18 11:13:33 2024 +0200

    remove team.html

commit febc6fb2f2680c6e332b2466fc1ec6b45319c8e8 (origin/ft/service-redesign)
Merge: 6539137 044e5de
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 15:04:15 2024 +0200

    resolved merge conflict on services file

commit 044e5de71e04929ce44502a88c58459c214f9b40
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 14:39:59 2024 +0200

    updated our services with the new stock products, we should be more profitable at this point

commit 6539137bdc3c31786063e1afa947366d5b48b689
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 14:00:27 2024 +0200

    updated our services page with more recent content

commit 583a938e9443f1fa9f7ea2f6568fa28af79ee825
Merge: 22b77ec 770d37e
Author: Varma Cephas <varmac231@gmail.com>
Date:   Tue Dec 17 13:49:46 2024 +0200

    Merge pull request #1 from varma-cephas/ft/bundle-2
    
    Ft/bundle 2

commit 770d37ea5cfa26616c933e48b43c54102bd636b2 (origin/ft/bundle-2, ft/bundle-2)
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 13:38:52 2024 +0200

    made changes in home, about and services files

commit bbdeae5585b3150210708acdf313f45dc6c77dcf (origin/dev, dev)
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 12:33:38 2024 +0200

    added home and about html files

commit 22b77ec260b5634879dc05a2ee9566ac00aba6b6
Author: varmac <varmac231@gmail.com>
Date:   Tue Dec 17 11:06:56 2024 +0200

    change branch name from master to main. create readme file
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/contact-page
Switched to branch 'ft/contact-page'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git cherry-pick be59dc041a34ec3b30c6603966bc7a2bc3254d27
[ft/contact-page 5305143] add team page and updated content
 Date: Wed Dec 18 11:24:02 2024 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our team page with descriptive content about how big our team is"
[ft/contact-page 6c1a00d] updated our team page with descriptive content about how big our team is
 1 file changed, 5 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/contact-page
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 750 bytes | 750.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/contact-page
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch faq.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "add our frequently asked questions page and added some content."
[ft/faq-page b1c0cb8] add our frequently asked questions page and added some content.
 1 file changed, 21 insertions(+)
 create mode 100644 faq.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/faq-page
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 522 bytes | 522.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/faq-page
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git revert be59dc041a34ec3b30c6603966bc7a2bc3254d27
CONFLICT (modify/delete): team.html deleted in parent of be59dc0 (add team page and updated content) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert be59dc0... add team page and updated content
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
gymumuco@umucos-iMac-2 gitExercise1-B1 % git revert be59dc041a34ec3b30c6603966bc7a2bc3254d27
CONFLICT (modify/delete): team.html deleted in parent of be59dc0 (add team page and updated content) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert be59dc0... add team page and updated content
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "removed the extra content added to our team page content and cleaned up file"
[ft/faq-page 3504830] removed the extra content added to our team page content and cleaned up file
 1 file changed, 5 deletions(-)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/faq-page
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 316 bytes | 316.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
To github.com:varma-cephas/gitExercise1-B1.git
   b1c0cb8..3504830  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push  origin ft/faq-page 
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Everything up-to-date
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```

### Exercise 2

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .               
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated about home and service page with additional content"
[main c392330] updated about home and service page with additional content
 3 files changed, 23 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 861 bytes | 861.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
To github.com:varma-cephas/gitExercise1-B1.git
   4b8164b..c392330  main -> main
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our home page with some content about the maintenance about our page"
[ft/home-page-redesign 72fba28] updated our home page with some content about the maintenance about our page
 1 file changed, 3 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin ft/ 
fatal: invalid refspec 'ft/'
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin ft/
fatal: invalid refspec 'ft/'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/home-page-redesign
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.90 KiB | 1.90 MiB/s, done.
Total 14 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/home-page-redesign
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```

##  Bundle 4

### Exercise 1

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git remote -v
origin	git@github.com:varma-cephas/gitExercise1-B1.git (fetch)
origin	git@github.com:varma-cephas/gitExercise1-B1.git (push)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git remote add git-copy git@github.com:varma-cephas/gitExercise-B4.git
gymumuco@umucos-iMac-2 gitExercise1-B1 % git remote -v
git-copy	git@github.com:varma-cephas/gitExercise-B4.git (fetch)
git-copy	git@github.com:varma-cephas/gitExercise-B4.git (push)
origin	git@github.com:varma-cephas/gitExercise1-B1.git (fetch)
origin	git@github.com:varma-cephas/gitExercise1-B1.git (push)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .                  
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "updated our home page with our annual earning for the year 2024" 
[main f0b1f62] updated our home page with our annual earning for the year 2024
 1 file changed, 2 insertions(+), 11 deletions(-)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 655 bytes | 655.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
To github.com:varma-cephas/gitExercise1-B1.git
   c392330..f0b1f62  main -> main
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push git-copy main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 27, done.
Counting objects: 100% (27/27), done.
Delta compression using up to 8 threads
Compressing objects: 100% (25/25), done.
Writing objects: 100% (27/27), 3.97 KiB | 3.97 MiB/s, done.
Total 27 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), done.
To github.com:varma-cephas/gitExercise-B4.git
 * [new branch]      main -> main
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```

### Exercise 2

```bash
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/footer
Switched to a new branch 'ft/footer'
gymumuco@umucos-iMac-2 gitExercise1-B1 % touch footer.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "add footer page and made changes to the rest of our page content" 
[ft/footer 33ac20c] add footer page and made changes to the rest of our page content
 4 files changed, 15 insertions(+)
 create mode 100644 footer.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "udpdate our home, about, services, and about with new content about the new services and important dates"
[ft/footer 4704697] udpdate our home, about, services, and about with new content about the new services and important dates
 4 files changed, 38 insertions(+)
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/footer
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (12/12), done.
Writing objects: 100% (12/12), 2.10 KiB | 2.10 MiB/s, done.
Total 12 (delta 5), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), done.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/footer
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout main
Switched to branch 'main'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
gymumuco@umucos-iMac-2 gitExercise1-B1 % git merge --squash ft/footer
Updating f0b1f62..4704697
Fast-forward
Squash commit -- not updating HEAD
 about.html    | 10 ++++++++++
 footer.html   | 18 ++++++++++++++++++
 home.html     |  8 ++++++++
 services.html | 17 +++++++++++++++++
 4 files changed, 53 insertions(+)
 create mode 100644 footer.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git add .
gymumuco@umucos-iMac-2 gitExercise1-B1 % git commit -m "footer changes squashing was amazing to see"
[ft/squashing cfb71f4] footer changes squashing was amazing to see
 4 files changed, 53 insertions(+)
 create mode 100644 footer.html
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push [-
zsh: bad pattern: [-
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
gymumuco@umucos-iMac-2 gitExercise1-B1 % git push --set-upstream origin ft/squashing
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.59 KiB | 1.59 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: This repository moved. Please use the new location:
remote:   git@github.com:varma-cephas/gitExercises.git
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/varma-cephas/gitExercises/pull/new/ft/squashing
remote: 
To github.com:varma-cephas/gitExercise1-B1.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.
gymumuco@umucos-iMac-2 gitExercise1-B1 % 
```

## Bundle 5

### Exercise 2

```bash
gymumuco@umucos-iMac-2 dec2024 % git clone git@github.com:varma-cephas/git-cafe-exercise.git
Cloning into 'git-cafe-exercise'...
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
remote: Enumerating objects: 107, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 107 (delta 5), reused 4 (delta 4), pack-reused 92 (from 1)
Receiving objects: 100% (107/107), 1.95 MiB | 510.00 KiB/s, done.
Resolving deltas: 100% (5/5), done.
gymumuco@umucos-iMac-2 dec2024 % cd git-cafe-exercise 
gymumuco@umucos-iMac-2 git-cafe-exercise % 
gymumuco@umucos-iMac-2 git-cafe-exercise % git remote -v
origin	git@github.com:varma-cephas/git-cafe-exercise.git (fetch)
origin	git@github.com:varma-cephas/git-cafe-exercise.git (push)
gymumuco@umucos-iMac-2 git-cafe-exercise % git add .
gymumuco@umucos-iMac-2 git-cafe-exercise % git commit -m "changed text in index file from our place to restaurant"
[main 99d11c5] changed text in index file from our place to restaurant
 1 file changed, 1 insertion(+), 1 deletion(-)
gymumuco@umucos-iMac-2 git-cafe-exercise % git push origin main
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 339 bytes | 339.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:varma-cephas/git-cafe-exercise.git
   d1d3f9c..99d11c5  main -> main
```

## Bundle 6

### Exercise 1

```bash
gymumuco@umucos-iMac-2 git-cafe-exercise % git checkout -b ft/menu-page
Switched to a new branch 'ft/menu-page'
gymumuco@umucos-iMac-2 git-cafe-exercise % touch menu.html
gymumuco@umucos-iMac-2 git-cafe-exercise % git add .
gymumuco@umucos-iMac-2 git-cafe-exercise % git commit -m "added new menu page and changes related"
[ft/menu-page 9577fc6] added new menu page and changes related
 1 file changed, 63 insertions(+)
 create mode 100644 menu.html
gymumuco@umucos-iMac-2 git-cafe-exercise % git push --set-upstream origin ft/menu-page
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 835 bytes | 835.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/menu-page' on GitHub by visiting:
remote:      https://github.com/varma-cephas/git-cafe-exercise/pull/new/ft/menu-page
remote: 
To github.com:varma-cephas/git-cafe-exercise.git
 * [new branch]      ft/menu-page -> ft/menu-page
branch 'ft/menu-page' set up to track 'origin/ft/menu-page'.
gymumuco@umucos-iMac-2 git-cafe-exercise % 
```

### Exercise 2

```bash
gymumuco@umucos-iMac-2 git-cafe-exercise % git checkout -b bugfix/change-title
Switched to a new branch 'bugfix/change-title'
gymumuco@umucos-iMac-2 git-cafe-exercise % mv index-4.html git status
mv: status is not a directory
gymumuco@umucos-iMac-2 git-cafe-exercise % git status
On branch bugfix/change-title
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index-4.html

no changes added to commit (use "git add" and/or "git commit -a")
gymumuco@umucos-iMac-2 git-cafe-exercise % git add .
gymumuco@umucos-iMac-2 git-cafe-exercise % git commit -m "changed title for index-4.html file to Contact"
[bugfix/change-title f657e18] changed title for index-4.html file to Contact
 1 file changed, 1 insertion(+), 1 deletion(-)
gymumuco@umucos-iMac-2 git-cafe-exercise % git push --set-upstream origin bugfix/change-title
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'bugfix/change-title' on GitHub by visiting:
remote:      https://github.com/varma-cephas/git-cafe-exercise/pull/new/bugfix/change-title
remote: 
To github.com:varma-cephas/git-cafe-exercise.git
 * [new branch]      bugfix/change-title -> bugfix/change-title
branch 'bugfix/change-title' set up to track 'origin/bugfix/change-title'.
gymumuco@umucos-iMac-2 git-cafe-exercise % git push --set-upstream origin bugfix/change-title
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 315 bytes | 315.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'bugfix/change-title' on GitHub by visiting:
remote:      https://github.com/varma-cephas/git-cafe-exercise/pull/new/bugfix/change-title
remote: 
To github.com:varma-cephas/git-cafe-exercise.git
 * [new branch]      bugfix/change-title -> bugfix/change-title
branch 'bugfix/change-title' set up to track 'origin/bugfix/change-title'.
gymumuco@umucos-iMac-2 git-cafe-exercise % 
```

### Exercise 3

```bash
gymumuco@umucos-iMac-2 git-cafe-exercise % git checkout -b hotfix/change-tel
Switched to a new branch 'hotfix/change-tel'
gymumuco@umucos-iMac-2 git-cafe-exercise % git status
On branch hotfix/change-tel
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index-4.html

no changes added to commit (use "git add" and/or "git commit -a")
gymumuco@umucos-iMac-2 git-cafe-exercise % git add .
gymumuco@umucos-iMac-2 git-cafe-exercise % git commit -m "change telephone number in index-4.html page to a new one"
[hotfix/change-tel ed73e8b] change telephone number in index-4.html page to a new one
 1 file changed, 1 insertion(+), 1 deletion(-)
gymumuco@umucos-iMac-2 git-cafe-exercise % git push --set-upstream origin hotfix/change-tel
Enter passphrase for key '/Users/gymumuco/.ssh/id_rsa': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 317 bytes | 317.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'hotfix/change-tel' on GitHub by visiting:
remote:      https://github.com/varma-cephas/git-cafe-exercise/pull/new/hotfix/change-tel
remote: 
To github.com:varma-cephas/git-cafe-exercise.git
 * [new branch]      hotfix/change-tel -> hotfix/change-tel
branch 'hotfix/change-tel' set up to track 'origin/hotfix/change-tel'.
gymumuco@umucos-iMac-2 git-cafe-exercise % 
```

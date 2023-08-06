

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ git log --oneline
2707715 (HEAD -> master) Sixth commit
a55e4bf Fifth Commit
7fe3707 fourth commit
e83efc5 fourth commit
2523ce7 second commit
8f8326e First commit

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ git checkout ^C

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ git checkout e83efc5
Note: checking out 'e83efc5'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>

HEAD is now at e83efc5 fourth commit

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit ((e83efc5...))
$ git checkout master
Previous HEAD position was e83efc5 fourth commit
Switched to branch 'master'

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   6.txt

no changes added to commit (use "git add" and/or "git commit -a")

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ git checkout -- 6.txt

DELL@WELCOME MINGW64 /d/GIT_2307/July/learninggit (master)
$ cd ..

DELL@WELCOME MINGW64 /d/GIT_2307/July
$ cd  ecommerceapp/

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp
$ git init
Initialized empty Git repository in D:/GIT_2307/July/ecommerceapp/.git/

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ mkdir src

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ mkdir test

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ mkdir docs

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ touch Readme.md

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ touch srd/main.py
touch: cannot touch 'srd/main.py': No such file or directory

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ touch src/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ touch test/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ touch docs/main.md

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        Readme.md
        docs/
        src/
        test/

nothing added to commit but untracked files present (use "git add" to track)

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git add -A

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   Readme.md
        new file:   docs/main.md
        new file:   src/main.py
        new file:   test/main.py


DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git commit -m "Intial folder structure"
[master (root-commit) 60695c0] Intial folder structure
 4 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Readme.md
 create mode 100644 docs/main.md
 create mode 100644 src/main.py
 create mode 100644 test/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git branch sprint-1

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git branch
* master
  sprint-1

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git checkout sprint-1
Switched to branch 'sprint-1'

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git branch
  master
* sprint-1

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ echo "Sprint 1 Started">>src/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git add .
warning: LF will be replaced by CRLF in src/main.py.
The file will have its original line endings in your working directory

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git commit -m " Feature 1 completed"
[sprint-1 55d0d6e]  Feature 1 completed
 1 file changed, 1 insertion(+)

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ echo "Sprint 1 Startd Testing ">>test/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git add .
warning: LF will be replaced by CRLF in test/main.py.
The file will have its original line endings in your working directory

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git commit -m "Feature 2 completed"
[sprint-1 c139a27] Feature 2 completed
 1 file changed, 1 insertion(+)

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git log
commit c139a2787354f1427c3b55f4a06fce9e60d249c4 (HEAD -> sprint-1)
Author: NAGA7022 <mailtonagab@gmail.com>
Date:   Sun Jul 30 15:46:23 2023 +0530

    Feature 2 completed

commit 55d0d6e4575b8cfe36fdbf14ed27460bd81cb136
Author: NAGA7022 <mailtonagab@gmail.com>
Date:   Sun Jul 30 15:44:52 2023 +0530

     Feature 1 completed

commit 60695c0d4f1ef1340b052f6f78bbcd02bec8f100 (master)
Author: NAGA7022 <mailtonagab@gmail.com>
Date:   Sun Jul 30 15:19:02 2023 +0530

    Intial folder structure

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ git checkout master
Switched to branch 'master'

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ cat src/main.py

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (master)
$ git checkout sprint-1
Switched to branch 'sprint-1'

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$ cat src/main.py
Sprint 1 Started

DELL@WELCOME MINGW64 /d/GIT_2307/July/ecommerceapp (sprint-1)
$
Need to change

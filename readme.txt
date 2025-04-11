# lab:
1- creat a new file called readme2.txt, then add and commit the changes
2- delete the original file readme.txt, then add and commit the changes
3- list all the the commits with git log
4- can you load the very first commit so you see the original readme.txt file?
5- what has happened to the new readme2.txt file?  


## steps


### step 1 : initialize a git repository

$ mkdir my-first-lab
$ cd my-first-lab
$ git init
Initialized empty Git repository in /home/mohamed/lab-git/.git/


### step 2 : creat a new file and commit it 

$ touch readme.txt 
$ echo "this is the first lab" >> readme.txt
$ git add readme.txt 
$ git commit -m "add readme.txt"
[master (root-commit) 96f2176] Add readme.txt
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt


### step 3 : creat a new file called readme2.txt, then add and commit the changes

$ touch readme2.txt
$ echo "hellow world" >> readme2.txt
$ git add readme2.txt 
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   readme2.txt
$ git commit -m "add new file readme2.txt"
[master edfe7b7] add new file readme2.txt
 1 file changed, 1 insertion(+)
 create mode 100644 readme2.txt
$ git commit -m "add new file readme2.txt"
[master edfe7b7] add new file readme2.txt
 1 file changed, 1 insertion(+)
 create mode 100644 readme2.txt

### step 3 : delete the original file readme.txt, then add and commit the changes

$ rm readme.txt
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	deleted:    readme.txt

no changes added to commit (use "git add" and/or "git commit -a")
$ git add readme.txt
$ git commit -m "deleted readme.txt"
[master eceb4e8] deleted readme.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 readme.txt


### step 4 : list all the the commits with git log

$ git log
commit eceb4e8d553c7eab73f49b731d642b4372d63a41 (HEAD -> master)
Author: mohamed tarek <mo.tarek1042000@gmail.com>
Date:   Fri Apr 11 15:55:24 2025 +0200

    deleted readme.txt

commit edfe7b7eadff5fba339e4c92702cc840435e1ec7
Author: mohamed tarek <mo.tarek1042000@gmail.com>
Date:   Fri Apr 11 15:51:31 2025 +0200

    add new file readme2.txt

commit 96f21768554624475a52785788d4eca84e243433
Author: mohamed tarek <mo.tarek1042000@gmail.com>
Date:   Fri Apr 11 15:44:34 2025 +0200

    Add readme.txt
 

### step 5 : can you load the very first commit so you see the original readme.txt file?

$ ls
readme2.txt
$ git checkout 96f21768554624475a52785788d4eca84e243433
HEAD is now at 96f2176 Add readme.txt
$ ls
readme.txt   


### step 6 : what has happened to the new readme2.txt file?

the project has returned to its original state before any changes were made 

# Git 
## What is git ?
####    It is source code version control system(VCS), helps to manage code changes in better manner.
#### It is distributed version control system.

## Why Git ?
#### It will be very difficult to handle changes in file and /or programs without git.
## What is version control system ?
* A software application which keeps tracks of code changes in efficient manner.
* Version control system is like adding new features and old features are removed.

## Need of version control:
* Multile peoples working in same software project.
* Need proper maintenance of stable(master) code and new features (probably unstable) code.
* Need of summary about who and what changes one did.
* Heavy code modification create challenges to maintain right source code.

## Different Version Control System:

```
                            Version Control Systems                           
                                   |
                                   |
        +--------------------------+----------------------+
        |                                                 |
        |                                                 |
       \|/                                               \|/
    Centralized                                       Distributed
        |-----> CVS                                       |-----> Bazaar(By Ubuntu)
        |-----> SUBVERSION                                |-----> GIT
        |-----> PERFORCE                                  |-----> Mercurial
                                                          |-----> FOSSIL


```
## Centralized vs Distributed Version control system:

* In Central version control system we perform update or commit directly to the central server repository.<br>
* In Distributed control system we perform commit to the ``local server repository``, from ``local server repository`` we perform push to the ``central server repository``.<br>
* While ``pulling`` we pull the data from ``central server repository`` to the ``local server repository``.<br>
* Distributed version control system is more fault tolerant.

```bash
Centralized control system

                Update
            +----------+     +----------+
           \|/ Commit  |     |          |
        +-----------+  +---->| System A |
        |           |        |          |
        |           |        |          |
        |  Server   |        +----------+   
        | Repository|
        |           |
        +-----------+
             /|\                   +------------+ 
              |     Update         |            |
              +------------------->|            |
                    Commit         |  System B  |
                                   |            |
                                   +------------+

```

```bash
Distributed Control system


                Push
         +-------------------+   +-----------------+        +-------------+
         |      Pull         |-->|                 |        |             |
        \|/                      |     Local       | Commit |             |
+-------------------+            |     Server      |<-------|   System A  |  
|                   |            |   Repository    |        |             |
|                   |            +-----------------+        +-------------+
|     Server        |
|     Repository    |
|                   |             +----------------+        +-------------+
|                   |             |                |        |             |
+-------------------+             |     Local      | Commit |             |
        /|\                       |     Server     |<------ |  System B   |
         |           Push         |   Repository   |        |             |
         +----------------------->|                |        |             | 
                    Pull          +----------------+        +-------------+

```


## Popular Git commands :

``clone:`` Download a repository which is hosted somewhere.<br>
``status:`` To check the status of github repository like what different files needs to push, files for updation. etc.<br>
``add:`` To add file in local repository.<br>
``commit:`` saves files in git.<br>
``config:`` Configure the github repository.<br>
``tag:`` It is used to tag an specific point in github repository.<br>
``push:`` upload git commits to remote repository.<br>
``pull:`` Download all the changes from remote reposiitory.<br>
``log:`` To see the history of the changes.<br>
``checkout:`` It is used for changing the the branch. <br>
``branch:`` to list, create and delete the branches.<br>
``merge:`` used to merge the two branches.<br>
``show:`` Shows one or more objects (blobs, trees, tags and commits).<br>
``stash:`` To store the uncommited data into temporary storage.<br>
## Stagging and unstagging

* ``Stagging:`` Staging the file will put the file into the staging area (index). The next git commit will transfer all items from staging area into the repository.<br>
eg.<br>
```bash
~$ git add <file name> # bringing the file at a place for commit. 
```
* ``Unstagging:`` 
Editing a versioned file on a local machine, git recognizes that file is modified - but it will not be automatically part of next commit hence therfore unstaged.<br>
In other words we can say Editing a versioned file makes the file modified, but unstaged.<br>
eg.<br>
```bash
~$ git reset HEAD <file name> # it will unstagged all the changes.

```
**git stash pop**:
Here user re-apply the previous commits by using git stash pop command. The popping option removes the changes from stash and applies them to the working file.


## Git config
* git config --globaluser.name \<user name\>
* git config --global user.email \<email of the user \>
* git config -l # to list config variables.


## Authenticating system for gitlab
* ssh-keygen -t ed25519 -C "comments".
* cat ~/.ssh/id_ed25519.pub.
* paste keys in gitlab: profile --> preference --> ssh keys

## Branching
* Generally while in development we perform all the work in ``dev`` branch or by creating some other branch. when everything is fine, it is merged to the master branch.
* Note :-> Please don't do your day to day activity in master branch.
* Creating a new branch:
    * ``git checkout -b <branch name>`` for creating and changing the branch.
    * ``git branch`` to create a new branch.
    * ``git checkout <branch name>`` to change the branch.
    * ``git push --set-upstream origin <current branch name>`` to push, if current branch has no upstream branch.
    * ``git branch -d <branch name>`` for deleting the branch.
    *  Merging the branch
    ```bash
    ~$ git branch master # to change the branch to master branch.
    ~$ git merge <branch name> # to merge the branch.
    ```

```bash
master [62c2]----->[8e97]---->[7216]---->[bef8]---->[bfc1]
        |     commit                                /|\ |
        |                                            |  |
        +------->[8e97]----->[34f7]------------------+  |
          checkout                        merge         |
         /branch                                       \|/
                                                       [416e]

```

    
## Git diff
* ``git diff`` is used for checking the differences between uncommited file and current file.



===============================End of Documents=================================

<center><h1>Thanks for reading!</h1></center>

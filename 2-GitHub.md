## 1. What is Git?
=> Git is a free open source distributed version control system widely used for tracking changes in source code during software development. It allows multiple developers to work on the same project simultaneously, keeping track of every individual contribution. <br>

### It is used for:
1. Tracking code changes <br>
2. Tracking who made changes <br>
3. Coding collaboration 


## 2. What is GitHub?
=> GitHub is an online software development platform. It's used for storing, tracking, and collaborating on software projects. It makes it easy for developers to share code files and collaborate with fellow developers on open-source projects. GitHub also serves as a social networking site where developers can openly network, collaborate, and pitch their work.

### What does Git do?
* Manage projects with __Repositories.__
* __Clone__ a project to work on local device/copy.
* Control and track changes with __Staging__ and __Committing.__
* __Branch__ and __Merge__ to allow work on different parts and versions of a project.
* __Pull__ the latest version of the project to a local copy.
* __Push__ local updates to the main project.

## Git Basics Commands:

* __git --version:__ To check if Git is properly installed and displays version.

* __git --help:__ Take help from the Git help section for different commands and other errors. It displays all options use with git.

* __git init:__ Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.

* __git clone [url]:__ Creates a copy of an existing repository on your local machine.
<br>

* __git config --global user.name <"name">:__ Sets configuration values for your name on git. <br> Define author name to be used for all commits in current repo. Devs commonly use ---global flag to set config options for current user.
* __git config --global user.email <"email">:__ Sets configuration calues for your user email on git.
* __git config --global --edit:__ Open the global configuration file in a text editor for manual editing.

* __git config --list:__ It displays list of credentials (name & email id) we set.
<br>

* __git add [file-name]:__ Add new or modified files in your repo to the Git staging area.
* __git add --all:__ Add all files of the current directory to the staging area.
<br>

* __git commit -m "message":__ Saves a snapshot of the staged changes with a descriptive message.
* __git commit -a -m "message":__ To add any of our tracked files to the stageing area and commit them by providing a message to remember.

* __git status:__ To see what's changed since the last commit. List which files are staged, unstaged and untracked.

* __git log:__ Display the entire commit history using the default format.
* __git reflog:__ Show a log of changes to the local repository's HEAD. Add __--relative-date__ flag to show date info or __--all__ to showsall refs. (Basically shows changes/history to the local repo by using all the commands.)
<br>

* __git diff:__ Show unstaged cahanges between your index and working directory..


## Undoing Changes Git Commands:

* __git revert [commit-branch]:__ Create new commit that undoes all of the changes made in <commit>, they apply it to the current branch.
<br>

* __git reset [file]:__ Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without oerwriting any changes.</li>
* __git restore --staged [file]:__ Remove <file> from the staging area.
  <br>
  
* __git rm --cached [file-name]:__ To remove staged file and make into unstaged.
  <br>

* __git clean -n:__ Shows which files would be removed from working directory. Use the __-f__ flag in plave of the __-n__ flag to execute the clean.


### Files/Directory Status in Git:
* __untracked:__ New file that git doesn't yet track.
* __modified:__ content of file was changed.
* __staged:__ Files is ready to be committed.
* __unmodified:__ Files there is no anything changed.


## Git Remote Repositories Commands:

* __git remote add [origin/name] [repo-url]:__ Create a new connection to remote repo. After adding a remote, you can use <origin/name> as a shortcut for <url> in other commands.

* __git remote -v:__ To verify remote connection.

* __git remote remove origin:__ Remove connection to remote repo.


## Git Push & Pull Command:

* __git push origin [branch]:__ Uploads your local (computer) commits to a remote (GitHub) repository.

* __git pull [origin/remote]:__ Fetches changes from a remote repository and merges them into your local branch.


## Working with Git Branches:
- In Git, a <b>branch</b> is a new/separate version of the main repository. <br>
- Branches allow you to work on different parts of a project without impacting the main branch. <br>
- When the work is complete, a branch can be merged wit the main project. <br>
- We can even switch between branches and work on different projects without them interfering with each other. <br>
- Branching in Git is very lightweignt and fast!


## Branch Commands:

* __git branch :__ To check current branch.

```console

[user@localhost]  git branch
                  * master
                    yash-branch

```

* __git branch -M main :__ To rename current selected branch

```console

[user@localhost]  git branch -M main
                  * main
                    yash-branch

```

* __git checkout <branch-name> :__ To navigate another branc.

```console

[user@localhost]  git checkout yash-branch
                    main
                  * yash-branch

```

* __git checkout -b <new-branch-name> :__ Create new branch and switch directly to that branch.

```console

[user@localhost]  git checkout -b new-branch
                    main
                    yash-branch
                  * new-branch

```

* __git branch -d <branch-name> :__ To delete branch.

```console

[user@localhost]  git branch -d new-branch
                  * main
                    yash-branch

```

## Merge Branches:
In git, merging branches means combining the changes from one branc into another. This is a fundamental operation in Git workflow, allowing developers to integrate changes made in different branches, such as feature branches, into a main development branch like <b>main</b> or <b>master</b>.

 __git merge :__ Combines changes from one branc into another.

```console

[user@localhost]  git merge yash-branch
                    Updating 09f4acd..dfa79db
                    Fast-forward
                     index.html | 2 +-
                     1 file changed, 1 insertion(+), 1 deletion(-)

```

### Merge Conflict:



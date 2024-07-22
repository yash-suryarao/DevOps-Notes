## 1. What is Git?
=> Git is a free open source distributed version control system widely used for tracking changes in source code during software development. It allows multiple developers to work on the same project simultaneously, keeping track of every individual contribution. <br>

### It is used for:
1. Tracking code changes <br>
2. Tracking who made changes <br>
3. Coding collaboration 


## 2. What is GitHub?
=> GitHub is an online software development platform. It's used for storing, tracking, and collaborating on software projects. It makes it easy for developers to share code files and collaborate with fellow developers on open-source projects. GitHub also serves as a social networking site where developers can openly network, collaborate, and pitch their work.

### What does Git do?
* Manage projects with <b>Repositories</b>.
* <b>Clone</b> a project to work on local device/copy.
* Control and track changes with <b>Staging</b> and <b>Committing.</b>
* <b>Branch</b> and <b>Merge</b> to allow work on different parts and versions of a project.
* <b>Pull</b> the latest version of the project to a local copy.
* <b>Push</b> local updates to the main project.

<br>

## Git Basics Commands:

* <b>git --version:</b>To check if Git is properly installed and displays version.

<br>

* <b>git --help:</b> Take help from the Git help section for different commands and other errors. It displays all options use with git.

<br>

* <b>git init:</b> Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.

<br>

* <b> git clone [url]:</b> Creates a copy of an existing repository on your local machine.

<br>

* <b> git config --global user.name <"name">:</b> Sets configuration values for your name on git. <br> Define author name to be used for all commits in current repo. Devs commonly use ---global flag to set config options for current user.
* <b> git config --global user.email <"email">:</b> Sets configuration calues for your user email on git.
* <b> git config --global --edit:</b> Open the global configuration file in a text editor for manual editing.

<br>
  
* <b> git config --list:</b> It displays list of credentials (name & email id) we set.

<br>

* <b> git add [file-name]:</b> Add new or modified files in your repo to the Git staging area.
* <b> git add --all:</b> Add all files of the current directory to the staging area.
  
<br>

* <b> git commit -m "message":</b> Saves a snapshot of the staged changes with a descriptive message.
* <b> git commit -a -m "message":</b> To add any of our tracked files to the stageing area and commit them by providing a message to remember.

<br>

* <b> git status:</b> To see what's changed since the last commit. <br> List which files are staged, unstaged and untracked.

<br>

* <b> git log:</b> Display the entire commit history using the default format.
* <b> git reflog:</b> Show a log of changes to the local repository's HEAD. Add <b>--relative-date</b> flag to show date info or <b>--all</b> to showsall refs. (Basically shows changes/history to the local repo by using all the commands.)

<br>

* <b> git diff:</b> Show unstaged cahanges between your index and working directory..


<br>

## Undoing Changes Git Commands:

<ul>
  <li><b> git revert [commit-branch]:</b> Create new commit that undoes all of the changes made in <commit>, they apply it to the current branch.</li>

<br>

  <li><b> git reset [file]: </b>Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without oerwriting any changes.</li>
  <li><b> git restore --staged [file]: </b>Remove <file> from the staging area.</li>

  <br>
  
  <li><b> git rm --cached [file-name]: </b>To remove staged file and make into unstaged.</li>

  <br>

  <li><b> git clean -n: </b>Shows which files would be removed from working directory. Use the <b>-f</b> flag in plave of the <b>-n</b> flag to execute the clean.</li>

</ul>

<br>

<h4> Files/Directory Status in Git: </h4>
<ul>
  <li><b>untracked :</b> New file that git doesn't yet track</li>
  <li><b>modified :</b> content of file was changed</li>
  <li><b>staged :</b> Files is ready to be committed</li>
  <li><b>unmodified :</b> files there is no anything changed</li>
</ul>

<br>

<h3> Git Remote Repositories Commands </h3>

<ul>

  <li><b> git remote add [origin/name] [repo-url] : </b>Create a new connection to remote repo. After adding a remote, you can use <origin/name> as a shortcut for <url> in other commands.</li>
  
  <br>
  
  <li><b> git remote -v : </b>To verify remote connection.</li>

  <li><b> git remote remove origin : </b>Remove connection to remote repo.</li>

</ul>

<br>
<h3> Git Push & Pull Command </h3>

  <li><b> git push origin [branch]:</b> Uploads your local (computer) commits to a remote (GitHub) repository.</li>

  <br>

  <li><b> git pull [origin/remote]: </b>Fetches changes from a remote repository and merges them into your local branch.</li>

  <br>

</ul>



<h3> Working with Git Branches: </h3>
- In Git, a <b>branch</b> is a new/separate version of the main repository. <br>
- Branches allow you to work on different parts of a project without impacting the main branch. <br>
- When the work is complete, a branch can be merged wit the main project. <br>
- We can even switch between branches and work on different projects without them interfering with each other. <br>
- Branching in Git is very lightweignt and fast! <br>


<h3>Branch Commands: </h3>
<ul>
  <li><b> git branch : </b>To check current branch</li>
</ul>

```console

[user@localhost]  git branch
                  * master
                    yash-branch

```

<ul>
  <li><b> git branch -M main : </b>To rename current selected branch</li>
</ul>

```console

[user@localhost]  git branch -M main
                  * main
                    yash-branch

```

<ul>
  <li><b> git checkout <branch-name> : </b>To navigate another branc</li>
</ul>

```console

[user@localhost]  git checkout yash-branch
                    main
                  * yash-branch

```
<ul>
  <li><b> git checkout -b <new-branch-name> : </b>Create new branch and switch directly to that branch</li>
</ul>

```console

[user@localhost]  git checkout -b new-branch
                    main
                    yash-branch
                  * new-branch

```
<ul>
  <li><b> git branch -d <branch-name> : </b>To delete branch</li>
</ul>

```console

[user@localhost]  git branch -d new-branch
                  * main
                    yash-branch

```

<h3> Merge Branches </h3>
In git, merging branches means combining the changes from one branc into another. This is a fundamental operation in Git workflow, allowing developers to integrate changes made in different branches, such as feature branches, into a main development branch like <b>main</b> or <b>master</b>.

<ul>
  <li><b> git merge : </b>Combines changes from one branc into another.</li>
</ul>

```console

[user@localhost]  git merge yash-branch
                    Updating 09f4acd..dfa79db
                    Fast-forward
                     index.html | 2 +-
                     1 file changed, 1 insertion(+), 1 deletion(-)

```

<h3> Merge Conflict </h3>



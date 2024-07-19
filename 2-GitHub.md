<h3> What is Git? </h3>
=> Git is a free open source distributed version control system widely used for tracking changes in source code during software development. It allows multiple developers to work on the same project simultaneously, keeping track of every individual contribution. <br><br>

It is used for:
1. Tracking code changes <br>
2. Tracking who made changes <br>
3. Coding collaboration 


<h3> 1. What is GitHub? </h3>
=> GitHub is an online software development platform. It's used for storing, tracking, and collaborating on software projects. It makes it easy for developers to share code files and collaborate with fellow developers on open-source projects. GitHub also serves as a social networking site where developers can openly network, collaborate, and pitch their work.


<h3> What does Git do?</h3>
<ul>
  <li> Manage projects with <b>Repositories</b </li>
  <li> <b>Clone</b> a project to work on local device/copy </li>
  <li> Control and track changes with <b>Staging</b> and <b>Committing</b> </li>
  <li> <b>Branch</b> and <b>Merge</b> to allow work on different parts and versions of a project </li>
  <li> <b>Pull</b> the latest version of the project to a local copy </li>
  <li> <b>Push</b> local updates to the main project </li>
</ul>


```console
  git --version
  git version 2.34.1

```
<h3> Git Commands: </h3>
<ul>
<li><b>git --version : </b>To check if Git is properly installed and displays version.</li>

<li><b>git help : </b>Take help from the Git help section for different commands and other errors.</li>

<li><b> git config : </b>To set the basic configurations on Git like your name and email.</li>
<li><b> git config --global user.name "Yash" : </b>Sets configuration values for your name on git.</li>
<li><b> git config --global user.email yash123@gmail.com : </b>Sets configuration calues for your user email on git.</li>
<li><b> git config --global color.ui true : </b>To see different colors on the command line for different outputs.</li>
<li><b> git config --list : </b>It displays list of credentials (name & email id) we set.</li>

<li><b> git status : </b>To see what's changed since the last commit.</li>

<li><b> git clone : </b>Creates a copy of an existing repository on your local machine.</li>

<li><b>git init : </b>Initializes a new Git repository in the current directory.</li>
<li><b> git remote add origin <link> : </b>Add new remote (GitHub repository)</li>
<li><b> git remote -v : </b>To verify remote</li>

<li><b> git branch : </b>To check current branch</li>
<li><b> git branch -M main : </b>To rename branch</li>

<li><b> git add <file-name>: </b>Add new or changed files in your directory to the Git staging area.</li>
<li><b> git add --all: </b>Add all files of the current directory to the staging area.</li>

<li><b> git commit -m "message": </b>Saves a snapshot of the staged changes with a descriptive message.</li>
<li><b> git commit -a -m "message": </b>To add any of our tracked files to the stageing area and commit them by providing a message to remember.</li>

<li><b> git log : </b>To check the history of commits for our reference.</li>
<li><b> git push origin main : </b>Uploads your local (computer) commits to a remote (GitHub) repository.</li>
<li><b> git pull : </b>Fetches changes from a remote repository and merges them into your local branch.</li>
<li><b> git branch : </b>Lists all branches in the repository.</li>
<li><b> git checkout : </b>Switches between branches.</li>
<li><b> git merge : </b>Combines changes from one branc into another.</li>

<li><b> git rm: </b>To remove files from working dir.</li>
<li><b> git rm --cached <file-name>: </b>To remove staged file and make into unstaged.</li>

<li><b> git diff: </b>To figure out what changes you made since the last commit.</li>
</ul>

<h3> Status in Git: </h3>
<ul>
  <li><b>untracked :</b> New file that git doesn't yet track</li>
  <li><b>modified :</b> content of file was changed</li>
  <li><b>staged :</b> Files is ready to be committed</li>
  <li><b>unmodified :</b> files there is no anything changed</li>
</ul>

<h3> Working with Git Branches: </h3>


<h3>Branch Commands: </h3>
<ul>
  <li><b> git branch : </b>To check current branch</li>
  <li><b> git branch -M main : </b>To rename branch</li>
  <li><b> git checkout <branch-name> : </b>To navigate</li>
  <li><b> git checkout -b <new-branch-name> : </b>Create new branch whitch directly to that branch</li>
  <li><b> git branch -d <branch-name> : </b>To delete branch</li>
</ul>

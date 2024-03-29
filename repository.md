﻿# Git Commands and Terminology <a name="top">


Return to Readme Page [Click Here](/README.md)

* [Repository](#repository)
* [Clone](#clone)
* [Fork](#fork)
* [Branch](#branch)
* [Commit](#commit)
* [Merge](#merge)
* [Checkout](#checkout)
* [Push](#push)
* [Pull](#pull)
* [Remote Add / Remove / Show ](#remote)
* [Status](#status)
* [Master Branch](#masterbranch)

___________________________________________________________________________________________________________________________________
  <a name="repository">
  
## Repository  
  
A repository generically refers to a central place where data is stored and maintained. A repository can be a place where multiple databases or files are located for distribution over a network, or a repository can be a location that is directly accessible to the user without having to travel across a network. 

Git is a program that tracks changes made to files. Once installed, Git can be initialized on a project to create a Git
repository. A Git repository is the .git/ folder inside a project. This repository tracks all changes made to files in your
project, building a history over time.

![](image/git_repos_image_source.png)

#### Example:
To start a new git repository using the command line:
1.	Create a directory to contain the project.
2.	Go into the new directory.
3.	Type git init .  -->To initialize the directory and creates a new Git repository
4.	Write some code.
5.	Type git add to add the files.
6.	Type git commit .

</a>

<a href="#top">Return to  Git Commands and Terminology</a>  

___________________________________________________________________________________________________________________________________
<a name="clone"> 
  
## Clone  

The git clone command copies an existing Git repository. This is sort of like SVN checkout, except the “working copy” is a full-fledged Git repository—it has its own history, manages its own files, and is a completely isolated environment from the original repository. 
The "clone" command downloads an existing Git repository [remote] to your local computer.
You will then have a full-blown, local version of that Git repo and can start working on the project.
Typically, the "original" repository is located on a remote server, often from a service like GitHub, Bitbucket, or GitLab). That remote repository's URL is then later referred to as the "origin".

![](image/clone_image.png)

#### Example:  

The following commands will download the project to a folder named after the Git repository ("Mini_Project_1" )

1. Repository Owner USERNAME: Web_Dev_IS601  

2. Git Hub Repository Project Name: Mini_Project_1 <br>
3. cd folder/to/clone-into/   ---> Change to the folder on your local directory that will contain the cloned repository.
4. Type Clone Command**:  git clone /https://github.com/Web_Dev_IS601/Mini_Project_1.git 

** SSH/HTTPS URL FORMAT :   git@name-of-git-host:username/project-name (SSH version) or [https://name-of-git-host/username/project-name] (HTTPS version).

<a href="#top">Return to  Git Commands and Terminology</a>  

___________________________________________________________________________________________________________________________________

<a name="fork">
  
  
# Fork
A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

Propose changes to someone else's project
A great example of using forks to propose changes is for bug fixes. Rather than logging an issue for a bug you've found, you can: 
*	Fork the repository.
*	Make the fix.
*	Submit a pull request to the project owner.

#### Example: 
Forking a repository is a two-step process.
1. On GitHub, navigate to the octocat/Spoon-Knife repository.
2. In the top-right corner of the page, click Fork {See image}.

![](image/fork_github.png)

A fork must be later synced with the upstream.
During git clone you actually copy the original repo. While a fork is just a request to clone the project and register under your username. Github also keeps track of relationship between the two repos. ... A "fork" is the typical nickname for a server-side clone (e.g. push to your fork before opening a pull request). 

![](image/fork.png)

## Difference between cloning and forking:
### (a) Cloning
By cloning a project, you are downloading a copy of that project to your local computer.
If you intend to collaborate on this project, you will only be able to publish / upload your changes if you have permission to do so (provided by the project's owner).  

### (b) Forking
By forking a project, you are creating your own copy of that project.
Since you are the owner of that project, you will be able to make any changes you like and add them (push them) back into the remote repository (the "fork"). You can only fork projects that are either public or where you have sufficient permissions.

<a href="#top">Return to  Git Commands and Terminology</a>
<br>
<br>
___________________________________________________________________________________________________________________________________
<a name="branch">  
  
# Branch

A branch in Git is simply a lightweight movable pointer to one of these commits. The default branch name in Git is master. As you initially make commits, you're given a master branch that points to the last commit you made. Every time you commit, it moves forward automatically.  
Branching is the practice of creating copies of programs or objects in development to work in parallel versions, retaining the original and working on the branch or making different changes to each. Each copy is considered a branch; the original program from which the branch is taken is referred to as the trunk, the baseline, the mainline or the master.
Branching is used in version control and software management to maintain stability while isolated changes are made to code. Branching facilitates the development of bug fixes, the addition of new capabilities and the integration of new versions after they have been tested in isolation.<br>
 
 In the image below, Branch1 and Branch2 are copies of the program in development which will allow the developers to work in parallel versions.
 
 ![](image/masterbranch2.png)
 
 
#### Example:
##### Scenario:  You are working on a project for Website development.You decide you are going to work on a new issue, namely issue10, pertaining to the website.  You create a branch so that you can do work on issue10. There are a few commits already on the master branch.  To create a new branch and switch to it, follow the following commands:</br></br>
$git branch issue10       -> This command creates new branch named “issue10” </br></br>
$git check out issue10     -> This command switches to the new branch “issue10” </br>
Abbreviated command: $git checkout -b issue10



<a href="#top">Return to  Git Commands and Terminology</a>

___________________________________________________________________________________________________________________________________
<a name="commit">  
  
# Commit

The "commit" command is used to save your changes to the local repository. You have to explicitly tell Git which changes you want to include in a commit before running the "git commit" command. This means that a file won't be automatically included in the next commit just because it was changed. Instead, you need to use the "git add" command to mark the desired changes for inclusion.<br><br>
A commit is not automatically transferred to the remote server, you need to use the "git add" command to mark the desired changes for inclusion. Following the "git add" command the changes will be placed in a staging area awaiting a "git commit" command {see diagram below}.   

![](image/commit.png)

<br>Using the "git commit" command only saves a new commit object in the local Git repository. <br><br>
Typing $git commit -m "<message>" at the command line is the proper syntax of the git commit command**. <br>

#### Example:
Assume you edited a file called hello-world.py and you are ready to commit it to the project’s history. First stage the file with git add:<br>
$git add hello-world.py<br>
Then commit the file:  
$git commit -m  “commit message”  
**  -m = Passing the -m option will forgo the text editor and prompt in-favor of an inline message.  
File hello-world.py will be saved in the local Git repository.

<a href="#top">Return to  Git Commands and Terminology</a>  


___________________________________________________________________________________________________________________________________
<a name="merge">  
  
# Merge

The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.
Git merge will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches.  There are two main ways Git will merge: Fast Forward and Three way.  


Fast Forward Merge  
A fast-forward merge can occur when there is a linear path between branches that you want to merge (see image below). </br>

 ![](image/fastforward_merge.png)


Three-Way Merge  
When there is not a linear path to the target branch, Git has no choice but to combine them via a three-way merge. This merge uses an extra commit to tie together the two branches (see image below).  

 ![](image/threeway_merge.png)



Merge command line syntax:  
$git merge "branch name"     ------>where "branch name" is the name of the branch that will be merged into the receiving branch. <br>

#### Example:
The code below creates a new branch, adds two commits to it, then integrates it into the main line with a fast-forward merge.  
#Start a new feature named issue10 		------>comment  
$git checkout -b issue10 master  
#Edit some files      				 ------>comment  
git add {file}  
git commit -m "The start of a feature"  
#Edit some files     				 ------>comment  
git add <file>  
git commit -m "The end of a feature"  
#Merge in the issue10 branch   ------>comment  
git checkout master  
git merge issue10				------>Merge a branch  
git branch -d issue10			   ---->Delete a branch  

<a href="#top">Return to  Git Commands and Terminology</a>  


__________________________________________________________________________________________________________________________________
<a name="checkout">  
  
# Checkout

In Git terms, a "checkout" is the act of switching between different versions of a target entity.  The git checkout command operates upon three distinct entities: files, commits, and branches.  

To checkout a specific commit, run the command: git checkout specific-commit-id  

To checkout an existing branch, run the command: git checkout BRANCH-NAME  

You can use the git checkout command to undo changes you’ve made to a file in your working directory. This will revert the file back to the version in HEAD: git checkout -- FILE-NAME


<a href="#top">Return to  Git Commands and Terminology</a>  

__________________________________________________________________________________________________________________________________

<a name="push">  
  
# Push

The git push command allows you to send (or push) the commits from your local branch in your local Git repository to the remote repository.
To be able to push to your remote repository, you must ensure that all your changes to the local repository are committed.

![](image/push.png)

Push command's syntax is as follows: git push {repo name} {branch name}
  
#### Example: Push to a Specific Remote Repository and Branch

Note: In order to push code, you must first clone a repository to your local machine.

**Type commands below :**   
#Once a repo is cloned, you'll be working inside of the default branch (the default is `master`) 
Type: git clone https://github.com/<git-user>/{repo-name}  
#change to the directory of your newly cloned repository.  
Type: cd {repo name}  
#make changes and stage your files. Repeat the `git add` command for each file, or use `git add .` to stage all  
Type: git add {filename}  
#now commit your code  
Type: git commit -m "added some changes to my repo!  
#push changes in `master` branch to github  
Type: git push origin master  
  
  
<a href="#top">Return to  Git Commands and Terminology</a>  

__________________________________________________________________________________________________________________________________
<a name="pull">  
  
# Pull
The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.  The git pull command is actually a combination of two other commands, git fetch followed by git merge. In the first stage of operation git pull will execute a git fetch scoped to the local branch that HEAD is pointed at. Once the content is downloaded, git pull will enter a merge workflow. A new merge commit will be-created and HEAD updated to point at the new commit.

git pull is a Git command used to update the local version of a repository from a remote.

It is one of the four commands that prompts network interaction by Git. By default, git pull does two things.

1.	Updates the current local working branch (currently checked out branch)
2.	Updates the remote tracking branches for all other branches.

git pull fetches (git fetch) the new commits and merges (git merge) these into your local branch.


![](image/pull.png)


Pull's syntax:  git pull {remote}

#### Example: 
--Fetch the specified remote’s copy of the current branch and immediately merge it into the local copy.
git pull origin master 


<a href="#top">Return to  Git Commands and Terminology</a>  

__________________________________________________________________________________________________________________________________
<a name="remote">  
  
# Remote Add/Remove/Show
### Add a Remote.
To add a new remote, use the git remote add command on the terminal, in the directory your repository is stored at.

The git remote add command takes two arguments:   
A remote name, for example, origin  
A remote URL, for example, https://github.com/user/repo.git  
#### Example:   
\$ git remote add origin https://github.com/user/repo.git  
\#Set a new remote  
\$ git remote -v  
\#Verify new remote  
\> origin  https://github.com/user/repo.git {fetch}  
\> origin  https://github.com/user/repo.git {push}  

### Remove a remote.
Use the git remote rm command to remove a remote URL from your repository. Note: git remote rm does not delete the remote repository from the server. It simply removes the remote and its references from your local repository.
#### Example: 
\$ git remote -v  
\#View current remotes  
\> origin  https://github.com/OWNER/REPOSITORY.git (fetch)  
\> origin  https://github.com/OWNER/REPOSITORY.git (push)  
\> destination  https://github.com/FORKER/REPOSITORY.git (fetch)  
\> destination  https://github.com/FORKER/REPOSITORY.git (push)

\$ git remote rm destination  
\# Remove remote  
\$ git remote -v  
\#Verify it's gone  
\> origin  https://github.com/OWNER/REPOSITORY.git (fetch)  
\> origin  https://github.com/OWNER/REPOSITORY.git (push)  

The destination remotes have been removed.
</br>
### Show a remote.  
Git-show - Shows one or more objects (blobs, trees, tags and commits).  
For commits it shows the log message and textual diff. It also presents the merge commit in a special format as produced by git diff-tree.  
For tags, it shows the tag message and the referenced objects.  
For trees, it shows the names (equivalent to git ls-tree with --name-only).  
For plain blobs, it shows the plain contents.  
The command takes options applicable to the git diff-tree command to control how the changes the commit introduces are shown.
Git show syntax: git show \<options> \<object>  

<a href="#top">Return to  Git Commands and Terminology</a>  

__________________________________________________________________________________________________________________________________
<a name="status">  
  
# Status
The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git. Status output does not show you any information regarding the committed project history.

#### Example: 
\$git status  
Lists which files are staged, unstaged, and untracked.  
Sample output of Git status:  
\# On branch master  
\# Changes to be committed:  
\# (use "git reset HEAD <file>..." to unstage)  
\#  
\#modified: hello.py  
\#  
\# Changes not staged for commit:  
\# (use "git add <file>..." to update what will be committed)  
\# (use "git checkout -- <file>..." to discard changes in working directory)  
\#  
\#modified: main.py  
\#  
\# Untracked files:  
\# (use "git add <file>..." to include in what will be committed)  
\#  
#hello.py  

<a href="#top">Return to  Git Commands and Terminology</a>  

__________________________________________________________________________________________________________________________________
<a name="masterbranch">  
  
# Master Branch
In Git, "master" is a naming convention for a branch. After cloning (downloading) a project from a remote server, the resulting local repository has a single local branch: the so-called "master" branch. This means that "master" can be seen as a repository's "default" branch.
A branch is essentially a unique set of code changes with a unique name. Each repository can have one or more branches. The main branch — the one where all changes eventually get merged back into, and is called master.</br>

Git will automatically create a master branch by default. Every next commit you make will go to the master branch until you decide to create and switch over to another branch.</br>

![](image/masterbranchlast_small.png)
  
In the above image we have a master branch and a pointer pointing at the last commit.  
<a href="#top">Return to  Git Commands and Terminology</a>
  
  
__________________________________________________________________________________________________________________________________
Return to Readme Page [Click Here](/README.md)



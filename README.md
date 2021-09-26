<a href="https://web1.eng.famu.fsu.edu/~kshoele/CTML/">
    <img src="https://github.com/CTML-Group/Git-tuto/blob/main/images/logo_CTML.png" alt="CTML logo" title="CTML" align="right" height="90" />
</a>    


<h1 align="center">
  Welcome to GitHub ! Test
</h1>


---
Let's start exploring GitHub together ..
# What is Git?

>>  Point to remember

It is a open-source <code>version control</code> tool that manages <code>different version</code> of your codes/files, <code>create a history of changes</code> and <code>tracks the changes</code>. Centralised and Distributed Version Control System (DVCS) are most common version control system existing in community.


---


## Centralised Version Control System (CVCS) 
- All the files, project files version history should be saved in central server
- To make changes you need to work locally once done push it to central server
- You will need access to central server
- You’ll only checkout the files you needed to modify therefore you won’t have complete version of code locally
- If something happens to central server, you may not be able to connect to your files
- Softwares such as <code>Subversion</code> uses centralised VCS
- Slow(er), network dependant, long urls, manual merges. To be used with care

## Distributed Version Control System (DVCS)  
- You’ll always have access to copy of entire project and its version history locally
- To make changes you can work both locally or remotely <a href="https://github.com/">github</a>, if you choose to work locally you will just need to connect to server for a few mins to sync your files to remote server
- You can access your files from anywhere across the globe
- Softwares such as <code>GitHub</code>, <code>Mercurial</code> etc. uses disttributed VCS
- Fast(er), network independent, often automatic merges. To be used early and often

## Snapshots are everything in GitHub
- Information is a set of snapshots, every committed change, Git takes another Snapshot
  - Snapshots are <code>full version of file</code> that has changed <code>not just changes to it</code>
- If we think about Subversion information is set of files plus <code>deltas of changes over time</code> – does not have full version
 <h1 align="center">
With GitHub you decide when to commit (i.e. to take snapshot) and of which files
</h1>


## Installation instructions

Install git using terminal or command prompt

```
Linux (Debian)>
sudo apt-get install git
```
```
Linux (Fedora)>
sudo yum install git
```
```
MacOS>
brew install git
```
```
Windows user can use this link>
[Using this link](https://git-scm.com/downloads)

```
```
Once you complete the download, you can verify its  installation using>
git  -- version or git version
```
Git is primarily a <code>command line</code> tool, but it also provides GUI based feature. If you would like to have <code>GUI feature</code> you can install
<a href="https://desktop.github.com/">GitHub Desktop</a> in your local PC or laptop

## Git Configuration

## `git config --global user`

`.name <name>`: Setup your name.
`.email <email>`: Setup your email.
Set your name and email that will be attached to your commits
```
Examples:
git config --global user.name "your-git-user-name"
git config --global user.email "your-git-email"
```
I'm sure most of us like alias, if so why not setting some alias as well to make our life even easier :smile:
Alias is a short form of frequently used commands

```
Some Examples, you can set it as you would prefer, (not mandatory)
git config --global alias.s status
git config --global alias.c commit
git config --global alias.br branch
git config --global alias.co checkout
git config --global alias.df diff
git config --global alias.lg 'log -p'
```

---
## Basic Terms in Git
<code>Repository</code>: It is the collection of all the files and history of those files, consist all your commits, often shortened as <code>repo</code>
		Repo can stay in local machine or remote server <a href="https://github.com/">github</a>, the act of copying remote repo to local machine is called <code>cloning</code>

## <code>Commit</code>: The act of creating snapshot; a project is made up of lots of commits, contains three piece of information
						- How the files have changed from previous version
						- A reference to commit that came before 
						- A commit id # also called hash code

<code>Pull</code>: Suppose you make some changes on your repo remotely that change will not be synced in your local machine, the process of downloading the remote commit to local machine is called pulling, we use “git pull command” conversely

<code>Push</code>: When you made changes locally that will not be reflected in remote server until you push them, we use “git push” command

## GitHub Workflow: Git works in <code>three</code> stages

<code>.git directory</code> (History) : Place where the metadata and object database of the project is stored, this is what's copied when you clone a repository.

1) <code>Working Directory</code>: Place where all the work takes place create, edit, delete, organize and save files, this is a version of the project that is checked out and placed on disk this is a file in the .git directory, that stores information about what will go into your next commit
	
2) <code>Staging Area</code>: Revised or modified files are staged, we add snapshots to the files in the staging area
	
3) <code>Git Repository</code>: Now we do commit that stores snapshot to your git repo and will be saved as version history



<h1>
	
[![](https://github.com/CTML-Group/Git-tuto/blob/main/images/git_workflow_architecture.JPG)]
	
</h1>


# GitHub Basic commands

---
## Getting started, and making changes
---
## `git init`

Start tracking a project in Git, this command creates the .git directory

---
## `git status`

Show the status of modified files in the working directory.

These can be _untracked_, _unstaged_ or _staged_ for commit.


* go into new folder
* do git init
* do git status
* no files
* touch readme.md
* git status - see untracked files

---
## `git add <files>`
Copy snapshots of modified files to the staging area, this command tracks new files
---

## `git commit`

This command save a snapshot of the staging area to the history as a commit

>>>  Point to remember:
 An important thing to note - is that every time a file changes, if you want to include that change with the next commit - you need to tell git to re-add it, as it is adding a snapshot of the file at the time the command is run.

-- edit file
-- git add
-- edit file again
-- need to add it again

## `Undo`

We are humans,  sometimes its normal to make mistakes i.e. to say NOT every commit is perfect 

Git provides some ways to work with your history using reset, revert, and checkout

## 'git revert <commit>'

>> Point to remember:

Git revert is one of the safer ways of to undo a changes, as it does not rewrite the history of your project. Git tries to figure out how to undo a change, and create a new commit for that change

---
## `git reset -- <files>`

This command copy files from the latest commit to staging area

Effectively undoes `git add <files>` by replacing files in the staging area by those last committed

Omit `<files>` to unstage everything.

>> Point to remember:

<code>git revert</code> does not move the project back to a previous state but <code>git reset</code> does. Git revert also allows you to revert changes at any point in history, where git reset can only work backwards from the current commit

Git reset can be considered a ' <code>very dangerous</code>' command also, as it is possible to lose work as you are unable to recover your original work

---

## `git checkout -- <files>`

This command copy files from the staging area to the working directory.

Omit `<files>` to throw away all local changes
	
## `git rm`

This command remove files from the working directory and the staging area

`--cached`: Remove files from the staging area only and keep them in the working directory.

---

## `git mv`

This command track the movement (renaming) of files

It essentially moves the file on the filesystem, `git rm`s and then `git add`s the moved file.

---
	
## `git clone <url>`

This command copies an existing Git repository to your local machine  and checks out a working copy of the latest version of the default branch

---

## `git diff`

This commad shows the exact lines added and removed in the working directory.

`--cached | --staged`: Compare your staged changes to those of your last commit.

---

## `git log`

This command helps you to browse and inspect the evolution of the project.


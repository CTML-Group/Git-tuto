<a href="https://web1.eng.famu.fsu.edu/~kshoele/CTML/">
    <img src="https://github.com/CTML-Group/Git-tuto/blob/main/images/logo_CTML.png" alt="CTML logo" title="CTML" align="right" height="90" />
</a>



<h1 align="center">
  Welcome to GitHub !!
</h1>


---
Let's start exploring GitHub together ..
# What is Git?

>> notes

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
Examples:
git config --global user.name "your-git-user-name"
git config --global user.email "your-git-email"









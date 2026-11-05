\# Git and GitHub Practice Report



\## Overview



This repository was used to practice the Git and GitHub workflow as part of Week 1 internship preparation at Aptic.



\## 1. Repository Setup



```cmd

E:

mkdir git-practice

cd git-practice

git init

```



Created a local Git repository in `E:\\git-practice`.



\## 2. Configure Git Identity



```cmd

git config --global user.name "Your Name"

git config --global user.email "your-email@example.com"

```



Configured the name and email used to identify commits.



\## 3. Create and Commit the README



```cmd

notepad README.md

git add README.md

git commit -m "Add project README"

```



Created the initial README and saved it as the first commit.



\## 4. Create a Feature Branch and Commit a File



```cmd

git switch -c feature/add-notes

notepad notes.txt

git add notes.txt

git commit -m "Add learning notes"

```



Created a feature branch, added `notes.txt`, and committed the change.



\## 5. Connect the Local Repository to GitHub



```cmd

git remote add origin https://github.com/apticasni/git-practice.git

git remote -v

```



Connected the local repository to the existing GitHub repository.



\## 6. Push the Feature Branch



```cmd

git push -u origin feature/add-notes

```



Published the feature branch to GitHub and configured upstream tracking.



\## 7. Create and Merge a Pull Request



On GitHub:



1\. Compared `feature/add-notes` with `master`.

2\. Created PR #1 titled \*\*Add learning notes\*\*.

3\. Reviewed the changed file and PR description.

4\. Merged the pull request into `master`.



\## 8. Update the Local Master Branch



```cmd

git switch master

git pull origin master

git log --oneline --graph --all

git status

```



Updated the local `master` branch and verified the merge history.



\## 9. Practice a Merge Conflict



Created two branches from `master`:



```cmd

git switch -c feature/update-readme

```



Edited and committed `README.md`:



```cmd

git add README.md

git commit -m "Update README with project purpose"

```



Created a second branch from `master`:



```cmd

git switch master

git switch -c feature/update-readme-team

```



Edited the same README file differently and committed:



```cmd

git add README.md

git commit -m "Update README with collaboration purpose"

```



Merged the second branch into the first:



```cmd

git switch feature/update-readme

git merge feature/update-readme-team

```



Resolved the conflict in `README.md` by retaining both intended lines, then completed the merge:



```cmd

git add README.md

git commit -m "Resolve README merge conflict"

git status

git log --oneline --graph --all

```



\## Skills Practiced



\- Initializing a Git repository.

\- Creating and editing files.

\- Staging and committing changes.

\- Creating and switching branches.

\- Connecting a local repository to GitHub.

\- Pushing branches and setting upstream tracking.

\- Creating and merging pull requests.

\- Updating local branches from remote.

\- Inspecting commit history.

\- Resolving merge conflicts.

\- Checking repository status.



\## Outcome



Successfully practiced a complete feature workflow using Git and GitHub, including branch creation, commits, pushing, pull requests, merging, and conflict resolution.




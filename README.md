# GIT Simplified and Explained
**GIT** is a system that tracks changes to our project files over time. It can record project changes and go back to a specific version of the tracked files, at any given point in time.  This system can be used by many people to efficiently work together and **collaborate on team projects**, where each developer can have their own version of the project, distributed on their computer. Later on, these individual versions of the project can be merged and adapted into the main version of the project.

## Steps to use GIT when working as a team
### 1- Configuring Your Name & Email:
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### 2.Initializing a local repository
```bash
git init
```

### 3. Staging and committing code
Committing is the process in which the changes are 'officially' added to the Git repository.
- While located inside the project folder in our terminal, we can type the following command to check the status of our repository:
```bash
git status
```
 It shows us which files have been changed.
 
 - add all the files inside the project folder to the staging area:
 ```bash
git add .
```
- commit the files from the staging area:
```bash
git commit -m "Commit message"
```
- To see all the commits that were made for our project, you can use the following command:
```bash
git log
```
The logs will show details for each commit, like the author name, the generated hash for the commit, date and time of the commit, and the commit message that we provided.
- To go back to a previous state of your project code that you committed, you can use the following command:
```bash
git checkout <commit-hash>
```
- To go back to the latest commit (the newest version of our project code), you can type this command:
```bash
git checkout master
```
### 5. Branches
A **branch** could be interpreted as an individual timeline of our project commits.
- You can create a new branch using the following command:
```bash
git branch <new-branch-name>
```
-To switch to a different branch, you use command:
```bash
git checkout <branch-name>
```
- To create a new branch and change to it at the same time, you can use the **-b** flag:
```bash
git checkout -b <new-branch-name>
```
- To list the branches:
```bash
git branch
```
- To go back to the master branch, use this command:
```bash
git checkout master
```
- You can merge branches in situations where you want to implement the code changes that you made in an individual branch to a different branch. For example, after you fully implemented and tested a new feature in your code, you would want to merge those changes to the stable branch of your project (which is usually the default **master** branch).To merge the changes from a different branch into your current branch, you can use this command:
```bash
git merge <branch-name>
```
- To delete a branch:
```bash
git branch -d <branch-name>
```

## 6- Working with remote repository:
- Navigate to your project directory using **cd**
- Create a remote repository for this project using this command:
```bash
git remote add origin <URL> 
```
The URL can be a github link to your project repository
- To upload the project files in our local repository to the remote, use:
```bash
git push -u origin master 
```
- To fetch a project from remote repository to your local. use:
```bash
git clone <cloning-URL>
```
-To check if your local repository up to date with the remote, use the following:
```bash
git fetch origin
git status
```
- To merge the changes from remote into your local repository:
```bash
git merge origin/master 
```
- Another way to recieve the changes into your local repository is the combination of both **fetch** and **merge**:
```bash
git pull
```
## 6- Merge conflicts:
This happens when two persons made changes to the same part(lines) of the code and both try to push changes to the remote repository. 


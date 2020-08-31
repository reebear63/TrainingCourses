# Git Starter Page #

"What do you call multiple developers working on the same project? - Merge Conflicts!"  


# History of Git # 
1991 - Änderungen am Linux Kernel via patches und archive files
2002 - Linux Kernel wird mit BitKeeper verwaltet (kostenlose Lizenz an die Linux Community)
2005 - Bruch zwischen Community und BitKeeper (verlangen nun Geld auch von der Community)

## Markdown ##
The Markdown Guide by Matt Cone
https://www.markdownguide.org/basic-syntax/

## Gwen Faraday - Git and GitHub for Beginners ##
https://www.youtube.com/watch?v=RGOj5yH7evk

What is Git?
a free and open-source version control system

What is Version Control?
The management of changes to documents, computer programs, large web sites, and other collections of information.

### git commands ###

init   - create a new directory and initialize it with git-specific functions  
clone  - bring a repository that is hosted somewhere like github into a folder on your local machine  
add    - track your files and changes in git, make git aware of a particular file  
>           git add .  
>           git add file1.md file2.md  
commit - save your files in git  
>            git commit -m "some message"  # -m stands for 'message'  
push   - upload git commits to a remote repo, like github  
>            git push  
>            git push origin master        #  
pull   - download changes from a remote repo to local machine, the opposite of push  
status - shows the status of changes as untracked, modified, or staged  
merge  - merges lines of development together  

### ssh keys ###
ssh-keygen -t rsa -b 4096 -C "email@example.com"

- public / private key-pair

---------------------------------------
https://guides.github.com/introduction/git-handbook/

**Example: Contribute to an existing repository**
```code=bash
# download a repository on GitHub.com to our machine
git clone https://github.com/me/repo.git

# change into the `repo` directory
cd repo

# create a new branch to store any new changes
git branch my-branch

# switch to that branch (line of development)
git checkout my-branch

# make changes, for example, edit `file1.md` and `file2.md` using the text editor

# stage the changed files
git add file1.md file2.md

# take a snapshot of the staging area (anything that's been added)
git commit -m "my snapshot"

# push changes to github
git push --set-upstream origin my-branch
```
**Example: Start a new repository and publish it to GitHub**
```code=bash
# create a new directory, and initialize it with git-specific functions
git init my-repo

# change into the `my-repo` directory
cd my-repo

# create the first file in the project
touch README.md

# git isn't aware of the file, stage it
git add README.md

# take a snapshot of the staging area
git commit -m "add README to initial commit"

# provide the path for the repository you created on github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

# push changes to github
git push --set-upstream origin main
```
**Example: contribute to an existing branch on GitHub**
```code=bash
# assumption: a project called `repo` already exists on the machine, and a new branch 
# has been pushed to GitHub.com since the last time changes were made locally

# change into the `repo` directory
cd repo

# update all remote tracking branches, and the currently checked out branch
git pull

# change into the existing branch called `feature-a`
git checkout feature-a

# make changes, for example, edit `file1.md` using the text editor

# stage the changed file
git add file1.md

# take a snapshot of the staging area
git commit -m "edit file1"

# push changes to github
git push
```

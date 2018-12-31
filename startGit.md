[Go back to contents](README.md/#Table-of-Contents)

# Creating a Git repository #

### Creating a new directory which is a git repository ###

1. This will print the version of git  
```shell
$ git --version
```

2. To create a repository:
```shell
$ git init repo_name
```
'repo_name' is the name of the repository that you want to create.
This is a directory with a lot of hidden files and folders.

3. To see all files in the 'repo_name' directory:
```shell
$ ls -a
. .. .git
```
- The -a flag shows all the hidden files and folders.
- The .git folder is your local repository. Inside that folder is all the history and the version control information about the project.


### Converting an existing directory into a git repository ###

```shell
$ git init
```
Without the project name, it will create a repo for the current directory.
__NOTE__: Name of the repository is *not* essential. As long as the .git folder exists, it will keep track of everything that happens.

---
**Everything important about the repository is contained in the .git folder.**
Even if someone deleted all the information in the directory (except the .git folder), we would still have all the information to restore all the work. 

This also means that if someone deleted the .git folder, all the version control information would be lost.
---


# Committing Changes #

! Always start the project with a good README file.

Before committing, a new file has to be added to the repository. Adding a file lets Git know that the file is important to the project and the changes in it should be tracked.

```shell
$ git add new_file
```
new_file -- name of the file which has to be added to the repository.

This functionality allows us to keep some files *outside* version control.
Not everything will be shared with others.

To commit a change, use the git commit command:
```shell
$ git commit file_name
```

This opens the Commit Message template in the default text editor. (By default, it is Nano)

```bash
GNU nano                FILE: .git/COMMIT_EDITMSG


# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# Committer: #PERSON WHO IS COMMITTING#
#
# On branch master
# 
# Initial commit
#
# Changes to be committed:
#    (use "git rm --cached<file>..." to unstage)
#
#    new file: #NAME OF THE FILE#
#

```

Commit message lets us know:
1. Who is making the commit.
2. On which branch we are working.
3. Brief discription of the changes we are making.

Best Practice : Keep the commit messages _Short_ and _Meaningful_.


### Important for people to know who is making the changes ###

```shell
$ git config --global user.name "My_Name"
$ git config --global user.email "My_Email"
```
My_Name -- name of the author
My_Email -- work email of the author

- Global flag lets git know that we would like these changes to be applied to all our repositories.


## After Making A Change To The File ##

Ask yourself: Should you commit it?
A simple rule of thumb: Is there a good commit message that you can use/

Important to commit everythime a good opportunity presents itself. The more number of commits, the more detailed the project history!

```shell
$ git commit -a -m "COMMIT MESSAGE"
```

-a flag is to commit all of the changes that git can find.
-m flag lets you add a commit message directly. Write the message directly after -m in quotes.


# The Staging Area #

It is an area where we can control precicely what we want to include in the commits.

```shell
$ git status
# shows the current branch
# if there are any changes that we need to commit
# or if there are any untracked files. 
```

Shows only the stuff which has changed since the last commit.

- Adding the untracked file, moves it to the "Staging Area".
- If any change is done to the already added file, then we have two options:
    + 'add' to add the changes to the staging area.
    + 'checkout' to discard the changes in the working directory.


# Exploring the History #

```shell
$ git log

# shows the log of all the commits
# starts with the most recent commits
```

Each log entry has:
1. A unique _commit identifier_ called a "hash".
2. Information about the author.
3. Date and time, when the code was committed.
4. Commit message.


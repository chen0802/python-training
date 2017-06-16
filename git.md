# Git Version Control

Git is a distributed version control system for software development. It allows us to keep track of and manage all of the different versions of our files for a project. It does this by keeping a history of all of the changes we have ever made to our files, and effectively works as a backup of all of our files. At any point, we can roll back any of the files that we are using with Git and revert back to a previous version.

Github is a hosting service for Git repositories (you can think of a repository as a directory/folder). Another way of looking at this is that Github is a hosting service for projects that use Git. Github allows us to share our projects with other people, and to allow other people to collaborate with us on our projects. 

We interact with Git locally on our computers, whereas we interact with Github through the Internet.

Mac users will use Git through the Terminal. Windows users can use Git through Git Bash, a command-line environment.

## Intializing a Git Repository Locally 

A Git repository is a collection of files whose changes are tracked by Git. There are a couple of different ways to create a new repository: 

* Initializing an empty, new local repository
* Downloading another repository (also known as *cloning* in git)

To initialize an empty, new local repository from the command line:

```bash 
git init my_new_repo # Initialize a new git repository called my_new_repo. 
git init # Initialize the current directory to be a git repository. 
```

## Add and Commit

Here is the standard Git workflow:

1.  add, remove, or edit any files in the repository
2.  add the modified files to the *index* (a file that Git uses to keep track of tracked files)
3.  commit those changes to history. 

The following are all commands that we would issue on the command line from within our Git repository. Note that any time we issue a Git command, it will be prefixed by `git`. 

```bash
git status # Will give you the the status of your repository (i.e. what 
           # files have been modified/created/added since your last commit). 

git add my_file.txt # Add the file my_file.txt to the staging area. 

git commit -m 'I committed!' # Commit all files in the index staging area with
                             # the commit message 'I committed'.
```

To simultaneously remove a file from Git and the file system, use `git rm`:

```bash
git rm my_file.txt
git commit -m "removing my_file.txt"
```

## Cloning

Instead of initializing an empty Git repository locally, we typically download an existing repository to use on our local machine. The process of creating a new local repository from an existing remote repository is known as *cloning* a repository.

To clone a repository, we simply issue the `git clone` command followed by a URL. 

```bash 
git clone URL # This will copy (clone) an existing repository from the given
              # URL, giving it the same name as the existing repository. Often
              # times this will be a URL that you grabbed from somebody's repo
              # on Github. 
```

## Push and Pull

To *pull* is to update the local version of the repository (e.g. on your laptop) with the latest version of the repository on the remote (e.g. on GitHub). 

To *push* is to update the remote version of the repository (e.g. on GitHub) with the latest local version of the repository (e.g. on your laptop). 

```bash 
git push # Apply any locally committed changes that aren't in the remote to the remote. 
git pull # Apply any changes in the remote that aren't in the local to the local.
```

If multiple people make changes to the same file simultaneously, that may create a *merge conflict*. We won't get into that here.

## Forking

*Forking* is like cloning, but forking occurs on Github, and is specific to GitHub (i.e. you don't fork on your local machine; there's no such concept). 

To fork, click the "Fork" icon near the top right of the repository page on github.com.

Forking creates your own personalized copy of the repository on your Github account. It's as if you cloned the repository, but you cloned it to your Github account (not to your local).  Now, if you would like to make changes locally, you would clone your forked repository.  Then any changes that you make will not be pushed to the original source of the fork, but rather to your personal copy on Github. 

Forking is used when you don't want to mess with the original repository source.

[**Back to Index**](README.md)

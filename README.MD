
# Assignment 1
Create a README.MD file and write answers to the following questions:




## Que 1: Can we have a global .gitignore?
#### Ans: 

As, a global .gitignore file stores all the files or directory that we want git to     ignore across all the repositories on the user's device or user account; which is stored in the user's home directory, we can have a global .gitignore.

## Que 2: How to find difference between two commits? 
#### Ans:

Ways to find the difference between two commits:
- #### Using git diff: 
    To use git diff, we need to know the sha of the commit initially. To find the sha of the commit, we can use git diff and then find the difference between two commits. git diff provides the comparison of the commits in two snapshots.
        
        Command:
        git log #To find sha of the commit
        git diff <sha> #To compare the commits
- #### Using gitk:
     gitk is a GUI tool that displays the commit history in a visual format. When we look at the history, we can select the commits we want to compare and compare them. This format makes the users compare the commits easily. 
        
        Command:
        gitk #To open the GUI and compare the commits 
## Que 3: Write difference between git add and git commit commands.
#### Ans:
 - #### git add:
            git add is a command to add/update the files or directory from the working directory to the staging area.(staging area is a temporary area)
- #### git commit:
            git commit is a command to add/update files from the staging area to local repositories. Files or directories cannot be committed without being added to the staging area. However we can used git commit -a command which stages and commits all the changes in a single line. After commiting the file or directory it is ready to be pushed in the remote repository.
## Que 4: How to unstage files?
#### Ans: 
To unstage files, we can use git reset. It resets the current HEAD to the previous commit. During this process the git history is changed.
Ways of unstaging files:
- To unstage all the files that have been staged:

        git reset HEAD
- To unstage a file for the staging area:

        git reset HEAD <fileName> 


## Que 5: How to revert a commit?
#### Ans:

A commit can be reverted using git revert. git revert creates a new commit that does not contain the changes made in the previous commit. To use git revert, we require the sha of the git(obtained using git log). It does not change the git history. 
Command:

    git log #To obtain sha of the commit
    git revert <sha>


## Que 6: Difference between revert and reset.
#### Ans:
 -  #### revert: 
    
    It creates a new commit that undoes the changes made by the previous commit. This way, git history is not changed.
   -  #### reset: 
    It undoes the changes made by the previous commit and resets the staging area. During this action, the git history is changed. It can be used to remove commits from the history.
 
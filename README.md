# learnableTask-week-2

1. EXPLAIN VERSION CONTROL
Version Control:
It is a system that tracks changes to the files or codes or projects over a time so that a specific version can be recalled later. Version control is a wise thing to use by the web designers, graphics designers, developers etc to keep every version of an image or layout or code. It allows you to revert selected files or entire project back to a previous state, compare changes over, see who last modified something that might be causing a problem, who introduced an issue and when and more. It enables multiple people to collaborate efficiently.

2. DIFFERENCE BETWEEN GIT AND GITHUB WITH THEIR EXPLANATIONS.
i. USAGE:
Git is use to control and manage changes made locally or across system by develpers. 

GitHub is use to store, share and collabrate on git repositories online.

ii. PURPOSE:
Git manages version control remotely and allows developers track, branch, comment, merge, revert changes and so on in a project.

GitHub provides a hosted service for Git repositories with features like issue tracking, project management, pull request, fork, etc.

iii. TYPE: 
Git is a command line tool which can work offline.

GitHub is web based platform and requires internet connection to work.

iv. DEFINITION:
Git is a distributed version control system (DVSC) used to track changes in files in the local directory.

GitHub is a cloud base platform that hosts git repositories  to ease collaboration.

3. LIST 3 GITHUB ALTERNATIVES.
i. Google Cloud Source Repositories.
ii. Bitbucket.
ii. AWS CodeCommit (Amazon web services).

4. EXPLAIN THE DIFFERENCE BETWEEN GIT FETCH AND GIT PULL.
They are both git command used for synchronization of local repository with a remote repository but they behave differently.

i. Git Fetch: 
this is a command that fetch all the changes on the server that you don't have yet and will not modify the working directory. It will let you to merge the data by yourself after getting the data. It is useful for reviewing differences before merging or incorprating changes.

Git Pull:
this is a command that look up what server and branch your current branch is tracking, fetch from the server and then they try to automaticaly merge in that remote branch. It is a combination of git fetch and git merge when you want to update your current branch with the latest changes from remote repositories immidiately.

5. EXPLAIN IN SIMPLE TERMS GIT REBASE AND THE COMMAND FOR IT.
Git Rebase:
this is a command that allows you to move or replay your changes from one branch to another, creating a clean history without unnecessary merge commits and this makes the project history easier to read and follow. 

EXAMPLE: 
lets say i have two branches;
main => branch housing the updates, 
develop => branch with my work.
To rebase my develop branch onto the latest version of main branch, use the commnand;
i. git checkout develop (it switch to development branch),
ii. git rebase main (rebase onto the main branch).

git will move all commits from develop branch and replay them on top of the latest commits from main branch.

In the case of error messages or conflicts, rebasing is paused by git and allows you fix the conflicts, stage the changes with 'git add.' and continue with the command line;
git rebase --continue

To abort or cancel rebase in any case use the  command line;
git rebase --abort

6. EXPLAIN IN SIMPLE TERMS GIT CHERRY PICK AND THE COMMAND FOR IT.
Git Cherry Pick:
This is command that allows you to take a specific commit from one branch and apply it to another branch. it is usefulin in fixing bugs or apply develop without bringing unrelated changes.

EXAMPLE: 
let say i have two branches;
develop => where i have 5 commits, 
main => where i want one of the commits. 
To pick a commit to apply: find the commit-id with the command 'git log' which will show the commit history with hash commit-id's like a1b2c3d. cherry pick command switches to the branch where you want to apply the commit.
i. git checkout main (switches to the main branch),
ii. git cherry-pick <commit-id> (apply the commit with id 'a1b2c3d').

In the case of error or conflicts, git will pause and ask you to fix them, after fixing them 'git add.' use to stage the resolved files and to to continue the cherry-pick use the command line;
git cheery-pick --continue

To abort or cancel cherry-pick in any case use the command line;
git cherry-pick --abort
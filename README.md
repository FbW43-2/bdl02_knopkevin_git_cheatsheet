# Git commands cheat-sheet: the most useful git commands
## 1. Navigate to your git project folder
Use `cd` to move between folders. For example:
```
cd workspace
cd bdl02_markopacak_git_cheatsheet
```
## 2. Check the status of the project
I can use these commands **anytime** to inspect my project.
- `git status`
    With `git status` I can see if some changes have happened and if some files are ready to be committed. 
    It gives me an overview of the project at that specific moment in time.
- `git log`
- `git diff`
## 3. Initialize a git project 
If any `git` command that we run gives the following output:
> fatal: not a git repository (or any of the parent directories): .git
it means that **we are not inside a git project**.
In this case we can:
1. Make sure that we are inside the right folder (and navigate to it, if necessary)
2. Initialize a git project
To initialize git, run 
```
git init
``` 
This command creates an empty Git repository. From now on, we can make changes to our files and permanently save those changes.
## 4. Save changes to files
1. `git add .` (or `git add -A`)
    `git add` tells Git that you want to include the latest changes in the next commit. However, changes are not actually recorded until you run `git commit`.
2. `git commit -m "Meaningful message here"`
    A commit is the Git equivalent of a "save". Commits can be thought of as snapshots of our project at a given point in time.
3. `git push`
    This command sends the committed changes to a server. It is used to upload local repository content to a remote repository.
## 5. Branches
1. `git branch "new branch name"`
    to create a new Branch
2. `git checkout "branch name"` to switch into another branch (in VSCode it happens automatically).
3. `git add .` or `git add -A` to save `git commit -m "message here..."` to commit and `git push --set-upstream origin` to push the new branch to github.
## 6. Merge
1. Assuming:
We are on a separate branch. Note: it can be checked by running `git branch -l`
We have added and committed all our changes.
We are now ready to merge our changes back to the main branch (which is usually master). It's time to:
2. Move to branch that you want to merge your changes on.
    E.g: `git checkout master`
    
    after checking out on master, its always good practice to pull the latest changes from the origin with:
    `git pull`
    
3. Merge the changes from the source branch (the one where we committed our changes on) with:
    `git merge my-username/source-branch`
4. Save our changes to the server
 `git push`
## 7. Fetch
```
git fetch
```
The `git fetch` command downloads commits, files, and refs from a remote repository into your local repo. Fetching is what you do when you want to see what everybody else has been working on.


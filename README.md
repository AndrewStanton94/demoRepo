demoRepo
========

These files are in markdown here are some links about the syntax:
    https://help.github.com/articles/markdown-basics/
    https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

#git commands
Adding to what was covered in the seminar

##add
If all files in changes not staged (the red ones) are to be added. Use the command `git add -A` where A = all.

##Checkout
Checkout can also be used to revert files to their state at last commit. `git checkout [filename]`
__This works until modified files have been added.__
I suggest that we use `add` when we have small changes to record. Then use `commit` and `push` when new features have been added, and at the end of coding sessions if there is only a single person working on the branch.

Another issue could be incomplete code due to interruptions. In this case:

1. Create a new branch: `git branch [branchName]`
2. Switch to new branch `git checkout [branchName]`
3. Use the `add` and `commit` commands as usual
4. There is a slight difference with pushing. The standard `push` command will fail as the branch doesn't exist on github at this time. The error message will show the correct code to enter. It will look like this:
    `git push --set-upstream origin [branchName]`
* Checking out any other branches will update files to the versions commited in those branches. Just checkout branchName to get back to your latest version.
5. Once the new branch has been completed. `add`, `commit` and `push` it.
* Each branch will need to be pushed separately.
6. Checkout to master (or parent branch) then merge the other branch in.

##Getting all branches
By default git clone will only clone the current branch. It does have info about the other branches however. This is displayed the first time you pull the repo after branch is added.
* Do `git branch -a` to see all branches (including remote)
* Then `git checkout -b localName origin/remoteName`

## Deleting branches
We probably won't be doing this much. Leaving them will be safer; but for reference:

### Deleting locally
`git branch -d branchName`
### Deleting remote
`git push origin --delete [branchName]`

## patching files from another branch
How to fetch files from another branch, use when not suitable for a merge.
Use this when the files exist on current branch. Gives a diff to before you merge
`git checkout --patch [branchName] [files]` (files space separated)
This command is used when the file doesn't exist in current branch (Or to overwrite?)
`git checkout [branchName] [files]`

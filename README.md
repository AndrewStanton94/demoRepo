demoRepo
========

These files are in markdown here are some links about the sysntax:
    https://help.github.com/articles/markdown-basics/
    https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

#git commands
Adding to what was covered in the seminar

##add
If all files in changes not staged (the red ones) are to be added. Use the command `git add -A` where A = all.

##Checkout
Checkout can also be used to revert files to their state at last commit. `git checkout [filename]`
__This works until modifed files have been added.__
I suggest that we use `add` when we have small changes to record. Then use `commit` and `push` when new features have been added, and at the end of coding sessions if there is only a single person working on the branch.

Another issue could be incomplete code due to interruptions. In this case:
1. Create a new branch: `git branch [branchName]`
2. Switch to new branch `git checkout [branchName]`
3. Use the `add` and `commit` commands as usual
4. There is a slight difference with pushing. The standard `push` commnand will fail as the branch doesn't exist on github at this time. The error message will show the correct code to enter. It will look like this:
    `git push --set-upstream origin [branchName]`
Checking out any other branches will update files to the versions commited in those branches. Just checkout branchName to get back to your latest version.
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

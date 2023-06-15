# Work_remote
Скоро я стану, как Илон Маск...

# Instruction for pull request
1. Sign in or sign up on github.com
2. Find a repository you like or the one that was provided to you. 
3. Create a fork of this repository (copying this repository to yourself)
4. Create an empty folder on your laptop
5. Open this folder in VScode 
6. Perform `git init` of this folder (in order for this folder to become a repository)
7. Check status with `git status`
8. Add the forked repository by copying the link on github.com and pasting it in `git remote add origin "LINK"`
9. Check that your 2 origins are the same (local and online repository) via `git remote -v`
10. Change the branch name from master to main with `git branch -m master main`
11. Perform `git pull` OR `git pull origin main`in order to pull all of the info from the Github online forked repository
12. Create a new branch with `git branch <branch_name>`
13. Switch to this new branch with `git checkout <branch_name>`
14. Include information that you need to this branch and save with Ctrl + C. 
15. Perform `git add` and `git commit`
16. Type `git push --set-upstream origin instr` in order for these new edits to appear in the forked repository online. 
17. Pull request
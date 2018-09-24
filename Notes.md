
* from [here](https://stackoverflow.com/questions/8762601/how-do-i-rename-my-git-master-branch-to-release)
* before the `git push --delete origin master`, go onto GitHub and change the default branch to be `dev`

```
git checkout -b dev master    # create and switch to the dev branch
git push -u origin dev        # push the dev branch to the remote and track it
git branch -d master              # delete local master
git push --delete origin master   # delete remote master
git remote prune origin           # delete the remote tracking branch
```

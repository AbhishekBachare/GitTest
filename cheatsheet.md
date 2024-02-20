# ================# Common Commands #==================

# clone git repo to local dir.:
git clone https://<utl_to_github_repo>

# get status on untracked files: 
git status

# add file for tracking using git:
git add <filename>

# add all files for tracking in current dir.:
git add .

# commit to local repo:
git commit -m "<commit_message>"

# add all + commit at same time:
git commit -a -m "<commit_message>"

# commands for setting user name and mail for git commit:
git config --global user.email "abc@mail.com"
git config --global user.name "abcname"

# log command:
git log --all --decorate --oneline --graph

# push to remote repo:
git push origin 
git push

# fetch & merge command:
git fetch
git merge origin

# pull & merge any updated from remote repo:
git pull 
git pull <repo_reference>

# get local logs:
git reflog

# show file modifications & update needed to be commited:
git diff <repo_reference>/<branch_name>
git diff origin/main

# rollback to the specific safepoint / commit:
git reset --hard <commit-id>
# below command will rollback to 2nd commit with id, it will rollcack all changed to this commit.
git reset --hard 0089frg

# revert / remove changes of specific commit:
git revert <commit_id>

# bring back all the changes done by commit (opposite to revert):
git cherry-pick <commit_id>

# ================# Git Branching #====================

# create branch:
git branch -c <branch_name>

# switch to branch:
git switch <branch_name>
# deprecated: 
git checkout <branch_name>

# create & switch to branch:
git switch -c <branch_name>

# merge a branch to main:
git merge <branch_name>

# list all branch and active branch:
git branch --list 

# push branch to remote repo:
git push origin HEAD:<branch_name>

# ================# Git Rebase #=======================

# use below git rebase to branch_name for linear commit history to reduce confusion. 
git rebase <branch_name>

# ================# Git Push local repo #==============

# GIT push local report to Github
# In project Root Directory run below command:
git init
# Dev / Create project files - add files using and make commit as per development.

# Rename master(default) branch to "main" for managing on github as per branch naming convenstions. 
git branch -M main

# Provide reference to github repo for local:
git remote add <repo_reference> <gihub_repo_URL>
# e.g:
git remote add origin <gihub_repo_URL>
# Note: Here "origin" is reference for future push & pull

# push local report main branch to upstream or github:
git push -u <repo_reference> <branch_name>
# e.g:
git push -u origin main

# ================# Git Stash #========================

# add current git index to stash:
git stash 

# to add current stash in git index & remove from stash:
git stash pop

# show stash: 
git stash show

# apply changes from specific stash:
git stash apply stash@{2}

# drop specific stash:
git stash drop stash@{2}

# clear stash all:
git stall clear

# git stash interactive change:
git stash push -p
# for untracked
git stash push -u 
git stash push -m <custome_message>

# ================# Git Squash #========================

# Git sqaush commit from Commit History:
git rebase -i <commit_id_to_start>
# replace pick with "squash", check using below git log command:
git log --oneline
# to check squashed commit, use reflog command:
git reflog 

========================================================
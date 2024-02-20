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

# get local logs:
git reflog

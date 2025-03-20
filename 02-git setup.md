# Setting up the Git repository

## To work with the tuto with versioning
1. Ensure that git is installed on your system
2. Create a Github account
3. Create a new repo (tuto, public, with a read file)
4. Github : settings/ssh keys/create new ssh key (default)
5. Copy the default ssh key from the host (workstation) in the key value
6. Download the repo (ssh link) into the workstation : `$ git clone git@github.com:rahimbtc1994/tuto.git`

## Configure Git
1. Configure user (name,email) : `$ git config --global user.name "..."` & `$ git config --global user.email "..."`

## Git
1. To shows the current state of your working directory and staging area `$ git status`
2. To shows the differences between files in various stages of the Git workflow `$ git diff`
3. Add changes to the commit : `$ git add .`
4. Commit : `$ git commit -m "update ..."`
5. Push : `$ git push origin master`
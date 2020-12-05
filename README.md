
## General

This repository doubles as an Obsidian vault. 

---
## Recipe Template

Please see [[Miso Salmon]] for an example of what a Recipe should look like. 

You can use the following tags and tag categories:

- Style #japanese #chinese #korean #mediterranean #mexican #indian #american
- Meat/protein type #fish #pork #beef #vegetarian #egg 
- Meal #breakfast #lunch #dinner #snack #dessert #drink
- Main or side #maindish #sidedish

---
---
## How to use Git (for Melissa)
These steps are for my fiancé, who has never used Git before.

---
##### Step 0.a -The set-up that Jeffrey did:
`cd ~/Documents/Personal/ChefJeff`

`git init`
- makes a `.git` file in this directory

`git add .`
- adds all the files I had made so far in the directory to the staging area called Index
- `.` is a shortcut that means "this current working directory" (i.e. the folder we are currently in)

`git commit -m "first commit"`
- commits all the changes in the staging area to HEAD, which is like the final staging area (but is still on your local computer)

`git branch -M main`
- changes name of the branch we are on (default is `master`) to be `main`

`git remote add origin https://github.com/jeffreyboschman/ChefJeff.git`
- connects this new local git repository that I just made to a remote server (I made one quickly on GitHub)
- now, we can push and pull changes from this remote server, and reference is with the name `origin` instead of `https://github.com/jeffreyboschman/ChefJeff.git` every time

`git push -u origin main`
- this command says "push the commits in the local branch named `main` to the remote named `origin`"
- now, all the stuff I just committed will be available to see on my github account online

---
##### Step 0.b - the set-up for Melissa: 
`<Command>+<Space Bar> Terminal`
- Opens the Terminal. This is a Command Line Interface

`git --version`
- This will show the version of git that is installed, verifying that you have it.
- You can do this command from any directory in Terminal

`git config --global user.name "Melissa L"`
`git config --global user.email "<your email>"`
- The very first time you use git, you need to set up your credentials:
	- The `--global` option tells Git to always use this information for anything you do on your system. If you omit `--global` or use `--local`, the configuration will be applied only to the current repository
	- You shouldn't have to do this anymore after the first time.
	- You can always check the configuration with:
	`git config --global --list`


`git config color.ui true`
- This is just a thing you can quickly do to show a more colourful git output on your terminal screen with certain commands

`cd <the folder where you want everything to be>`
- Now we want to go to a certain directory on your local computer. This is where we will put the files. 
- `cd` means "change directory". 
	- This is a UNIX command. All the Git commands are prefaced by `git`

`git clone https://github.com/jeffreyboschman/ChefJeff.git`
- To make a copy of the remote respository that I made and see it on your local computer for the first time, you need to "clone" it. 

`ls`
- The `ls` command means "list", as in "list the contents of this directory" 
	- This is another example of a UNIX command
---
##### Step 1 (for Melissa): 
Before you start working, you want to make sure you have the latest version of everything

`git pull`
- to update your local respository to the newest commit in the remote repository (i.e. make sure you have the latest version)
- This "fetches" and "merges" the remote changes to your local repository

---
##### Step 2 (for Melissa):

Now, you can edit the files, add new files, etc. When you have finished what you wanted to do, move to step 3 to update the remote repository with your local changes.

---
##### Step 3 (for Melissa):
Now you want to update the remote repository so it has all the changes you made. This is important because if Jeffrey wants to work on the project, your changes will be there. 

`git status`
- with this command you can see what files have been changed, and whether or not you have added these to the staging area

`git add .`
- adds all the changes you have made in your local repository to your local staging area
- remember, `.` is a UNIX shortcut that means "this current working directory" (i.e. the folder we are currently in)
	- this is most likely the command you will use

`git commit -m "<quick commit message>""`
- commits the changes you proposed in the staging area to HEAD. 
	- Now it is in the HEAD of your local working repository, but still has not been "pushed" to the remote repository
- For "quick commit message", some examples might be:
	- "added ramen recipe"
	- "changed miso salmon recipe"
	- "added quinoa recipe and chicken teriyaki video link"

`git push origin main`
- this will "push" the commits you made to to the remote repository.
- Now the changes will be reflected on the GitHub page, and Jeffrey can do his own `git pull` to see those changes on his local computer

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
## How to use git (for Melissa)
These steps are for my fiancé, who has never used git before.

Step 0: 
Make sure git is installed. 
`git --version`
	
The very first time you use git, you need to set up your credentials:
	`git config --global user.name "Melissa L"`
	`git config --global user.email "<your email>"`
- you shouldn't have to do this anymore after the first time. You can always check to make sure you're still "logged in" with:
		`something`
		
Step 0 (for Jeffrey):
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




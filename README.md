# lrrg
Little Red Riding Git. A simple game for git collaboration training.

Let's write (or re-write) the story of Little Red Riding Hood.

## Pre-requisites

* Internet connection
* Git is installed on the player's computer.
* Fork this repo into a remote repo that all players can contribute to.

## Basic play

In this game, two content collaborators work on a new website “Little Red Riding Git.”

In their website, they will tell the story of Little Red Riding Hood, and add a few twists.

(The game can be played by two people, or one person with two terminal sessions, simulating a multi-player experience.)

One player assumes the role or Little Red, and the other Granny.

Each player opens a terminal window, e.g. Git Bash.

Follow the command line script below, but feel free to improvise. 

Create a directory

`mkdir ~/lrrg`

Each player clones the forked repo, e.g.

`git clone git@github.com:mygithubaccount/lrrg.git little-red`

`cd little-red`

And

`git clone git@github.com:mygithubaccount/lrrg.git granny`

`cd granny`

Little Red will start first: 

`touch ch1.htm`
`ls`
`git status`
`vim ch1.htm`

Enter:
```
Chapter 1

<h1>Little Red Leaves Home</h1>

<p>Little Re opens the door and trips over the threshold.</p>
```
Save and exit the editor. 

Stage your changes:

`git add .`

`git status`

`git commit -m 'Start Chapter 1’`

`git status`

`git push origin master`

Now it's granny's turn:

`git pull`

`ls`

`git log`

`git show [sha]`

`git branch -a`

`git checkout -b granny`

`ls`

Make an update, e.g. "Little Red opens the door and slips on a banana."

`code ch1.htm`

Save and exit the editor. 

Stage your changes:

`git status`

`git a .`

`git status`

`git commit -m 'Add more drama'`

`git status`

`git push`

Now it's Little Red's turn

`git pull`

`git log`

`git log --all`

`git checkout granny`

`git diff master granny`

`git checkout master`

`git merge granny`

`git log`

`git status` 

I see my working directory is clean. This is because the merge pointed the master branch to the new commit added by Granny, and updated my working directory.

`code ch1.htm`

You have seen how simple it can be to work with the git CLI to perform basic version control operations in a collaboration scenario.

Please continue play to practice your commands and explore new ones.

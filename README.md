# lrrg
Little Red Riding Git. A simple game for git collaboration training.

Let's write (or re-write) the story of Little Red Riding Hood.

## Pre-requisites

* Git is installed on the player's computer.
* Fork this repo into a remote repo that all players can contribute to.

## Basic play

* Three players with roles:
  * Little Red
  * Granny
  * Wolf
* Players clone this repo
* Little Red is the maintainer, works in the master branch
* Granny creates a branch called "granny"
  * `git checkout -b granny`
* Wolf creates a branch called "wolf"
  * `git checkout -b wolf`
* There are five turns
* In each turn, players create 1-3 files, each having a step in their story. 
  * Prefix file names with chapter number and step, e.g. `1.1_`
  * Example `touch 1.1_little-red-leaves.home`
  * No need to add file content.
  * You can be creative with your file extension
* After creating your files, commit to git as a chapter in their story.
  * `git add .`
  * `git commit -m "C1 My Chapter Name"`
  * `git push` 
  * `git pull`
* After five turns, together we'll review the branch history
  * `git checkout master`
  * `git log --oneline --name-only`
  * Repeat for each branch
  * Finish off by showing the log as a graph for all branches
  * `git log --graph --all --oneline --decorate --name-only`
* Little Red merges the branches into master
  * `git checkout master`
  * `git merge granny`
  * `git merge wolf`

## Advanced play

_Ideas..._

* Cherry pick from branches
* 

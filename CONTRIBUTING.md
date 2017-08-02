# Welcome to a SESYNC Training Event

This document explains how to create and contribute to your own GitHub repository, including initializing the repository as a duplicate of [SESYNC-ci/handouts]. The steps below assume you will primarilly use the git version control system from with RStudio.

1. [Create a RSA key pair on your computerand GitHub.](#create-rsa-key-pair-in-rstudio-and-github)
1. [Import SESYNC-ci/handouts on GitHub.](#import-repository)
1. [Create a new project within RStudio.](#create-rstudio-project)
1. [Configure git.](#configure-git)

## Create RSA Key Pair in RStudio and GitHub

Follow [the instructions](http://adamwilson.us/RDataScience/GitSSHNotes.html#generating-a-ssh-key-in-rstudio) by Adam Wison.

## Import Repository

Use the repository importer with the "https://..." URL for [SEYSNC-ci/handouts]. Exclude large files if asked.

## Create RStudio Project

## Configure git

## Local Clone

First, let's make sure you keep the original version of this repository "upstream", so you can pull (i.e. download and merge) any changes made by your instructor. From a shell opened within your local clone, enter:

    git remote rename origin upstream

Next, create a repository on GitHub to use as the new "origin". While logged in to GitHub, use the "+" icon in the upper right to create a new repository. Give it a name but leave the repo empty&mdash;don't even check the box to add a README. Finally, link your remote GitHub repository to your local clone by adding the remote as "origin" using the URL copied from the green "Clone or download" button. From a shell opened within your local clone, enter:

    git remote add origin <URL>
	
After making commits, you can push them to your repo. The first time you do this, you'll need an extra option:

    git push -u origin master
    
The `-u origin` option sets up the origin to sync with the "master" branch of your local clone. Subsequently a simple `git push` will suffice. To merge changes from upstream (e.g. updates from your instructor), you can enter:

    git pull upstream master
   
You are now able to commit and push any changes you make locally to your own repo on GitHub, while also merging any changes your instructor makes upstream.

## GitHub Import

The GitHub "import" feature creates a duplicate of the handouts repository under your username on GitHub. You have full control over this copy, to clone, push, and add collaborators. Once you have created a local clone, for example, you'll be able to push commits up to your GitHub repository with a simple `git push`. To create the local clone, copy the URL from the green "Clone or download" button, open a shell where you want to create a new folder, and enter:

    git clone <URL>


It could also be useful to set up a link to the original [SESYNC-ci/handouts] repository, so you can pull (i.e. download and merge) any changes or additions from the instructor. With the shell opened to anywhere within your local clone, enter:

    git remote add upstream https://github.com/sesync-ci/handouts.git

To merge changes from "upstream", you can now execute `git pull upstream master` from a shell anytime to integrate new commits from [SESYNC-ci/handouts]. Be warned though, after your course is over the original repository could change dramatically for the next course!

## GitHub Fork

By forking from [SESYNC-ci/handouts] on GitHub, you have become the owner of a mirror of the handouts repository that automatically sets your mirror "downstream" of the original. You have full control over this copy, to clone, push, and add collaborators. Once you have created a local clone, for example, you'll be able to push commits up to your repository with a simple `git push`.

Your fork remains linked to the original repository, which you can use to update your repository with changes made by the instructor on [SESYNC-ci/handouts] if necessaryy. Issue a '[pull request](https://help.github.com/articles/about-pull-requests/)' directly from GitHub with the 'base fork' set to your fork and the 'head fork' set to [SESYNC-ci/handouts] (i.e. the reverse of the default settings for a new pull request). Then merge your pull request.

[SESYNC-ci/handouts]: https://github.com/sesync-ci/handouts

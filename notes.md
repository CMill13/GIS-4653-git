
These notes are summarized and excerpted from:
http://github.com/swcarpentry/bc/novice/git/

Version control is good because:

## Overview
* Nothing is ever lost, infinite undo
* Scientific provenance, "What was the code when I wrote that paper?"
* Who made what changes, where and when?
* Hard to overwrite people's improvements

## What is git?
* A **distributed** version control and source management system.
* Similar to SVN, cvs and Mercurial etc, but different in key ways.


How do we use git?

* We use it to track changes made to files in a particular directory.

## Git Local

* Configure git so it knows about you. `git config --global user.name "Jonah Duckles"`, `git config --global user.email "jduckles@ou.edu"`
* talk about git-bash and git
* `pwd` - print working directory
* `mkdir planets`
* `cd planets`
* Create a repository `git init .`
* What is a git repository, just a magic `.git` directory and a "working directory"
* Talk about two staged commits `git add` then `git commit`
* Use an editor, python IDE perhaps, save files to your `mycode` folder. Call it `mars.txt`
* Add some things you know about mars 
* `git status`
* `git add mars.txt`
* `git commit -m "About mars"`
* Make some more changes, save them
* `git status`
* `git add mars.txt`
* `git commit -m "more information"
* Make another set of changes
* `git status`
* `git add mars.txt`
* `git commit -m "further info about mars"
* This is your standard git workflow, use `git status` to check-in on files in a repository.  `git add` them to "stage" commits for commitment, then `git commit -m 'with a descriptive message'
* `git log`
* Lists revisions made to repo in reverse chronological order
    * included full identifier
    * author
    * when created
    * the commit message
* What do we see when we run `ls`?
* Make some more changes to the file.
* `git diff`
* two stage commit is a PITA!!! Why?
    * We may want to commit "threads" of changes across our files.  Say we make changes to improve a particular data preparation routine, and changes related to our core algorithm.  It makes sense to commit these each as independent commits, the two stage commit allows us to do just that.  We only `git add` the things that are going to be part of a certain commit.
* `git diff HEAD~1`
* Why the `~`?
* `git diff HEAD~2`

#### Key Points
*   Use `git config` to configure a user name, email address, editor, and other preferences once per machine.
*   `git init` initializes a repository.
*   `git status` shows the status of a repository.
*   Files can be stored in a project's working directory (which users see),
    the staging area (where the next commit is being built up)
    and the local repository (where snapshots are permanently recorded).
*   `git add` puts files in the staging area.
*   `git commit` creates a snapshot of the staging area in the local repository.
*   Always write a log message when committing changes.
*   `git diff` displays differences between revisions.

### Git Remote

* Go to http://www.github.com and make an account.
* Lets make a repository called `planets`
* This makes a new repository on github which happens to be named the same as our local repository, running a `git init` in it.
* Connecting the repositories: back at the commandline type `git remote add origin https://github.com/yourusername/learngit.git`.  Where we say `origin` it can be any word, it is just a name for that particular "remote".
* `git remote -v` shows us our remote setup.
* `git push origin master`
* `git pull origin master`

* Create a new repo on github...then clone it.









+++
author = "Arno V"
date = 2020-11-13T20:00:00Z
hero = "/images/yancy-min-842ofhc6mai-unsplash.jpg"
title = "My first git usage at work"
type = "blog"

+++
# The few things I know about git

At work, people use **gerrit** ([https://www.gerritcodereview.com/](https://www.gerritcodereview.com/ "gerrit")). I'm not too sure how it differs from the classic version control & Github, so let's go ahead anyway.

### Seeing past changes and where you're at

To do this, and have a gui view on past changes, head to the terminal and type

    $ gitk --all

This should open a window telling you things. Not sure yet what in the details. But keep that in mind.

### Saving your local changes

Usually when you use git, there are two versions of your code: the **local** (what's on your PC), and the **remote** (what's hosted on gerrit, or github for example). You usually want them to match in the end, but that's not always easy.

The most important is that you do not lose what you've been coding, you can save your progress through the command

    $ git stash

### Making sure you're updated with the remote

Now, one usually proceeds by taking the code that's on the remote server, and copying on top of what you have locally. You're not afraid to lose things, because you've just stashed your progress. To copy the remotely hosted content on your remote, type

    $ git pull --rebase

This assume the branch is already known. If someone tells you the branch / you know the branch name but the above command does not work, do the following (works for gerrit)

    $ git 
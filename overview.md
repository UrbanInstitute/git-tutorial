#An Overview

##What is git? test test test test

Git is a piece of software that helps organize and track changes to files over time (usually text based files, like code), and helps multiple users work on the same projects, without stepping on each others' toes. Git is run from the command line (by default the [Terminal](http://en.wikipedia.org/wiki/Terminal_%28OS_X%29) on Macs and the [Command Prompt](http://en.wikipedia.org/wiki/Cmd.exe) on PCs), usually by running `git`, followed by another key word, then often followed by various options.

sublimerge test

##What is github?

Github is a website (you're on it now!) that provides a visual interface for git, as well as hosting the files that make up a project. *One* version of these files is hosted on github servers (called the *remote* version), but in almost every case there are many other versions on various other computers (called *clones*). For example, on my computer at work I have a version of these files, and another version on my computer at home. When you follow these tutorials, you'll have your own version(s). As we work on the files, at various times we will sync them up with the remote version that is on github, by **pushing** the changes we make to github and **pulling** down the changes other users make to the remote version.

I go over a few nice github features in [another document](working.md), but most of what we'll talk about is specific to git, not github. Almost all of the functions and commands we talk about are still valid when using services such as [bitbucket](https://bitbucket.org/) or [gitlab](https://about.gitlab.com/).

Many [open-source software projects](http://en.wikipedia.org/wiki/Free_and_open-source_software) are hosted on github (or bitbucket and other git hosting services). Personally, I am a passionate proponent for open-source software, working in the open, and the open data movement. I'd be happy to chat more about the whys and the hows of open-source development, and [many](https://github.com/18F/open-source-policy/blob/master/policy.md) [other](http://www.gnu.org/gnu/manifesto.html) [folks](https://okfn.org/opendata/why-open-data/) have written more eloquently and thorougly than I ever could.

Most software developers write their code using git, sometimes in public, sometimes in private (charging for private hosting is one way github makes money). The more you work with git, the more invaluable it will become to you.

##Overview
In the [main tutorial](working.md), there's a ton of information and steps to follow. Here, I'll just give a quick overview of the fundamental git workflow. Let's say you're working on some files, on your local clone, and want to sync up with the remote version on github:

###git add
Flag certain file(s) as ready to be synced

###git commit
Lump all your changes together, and write a message describing the changes

###git pull
Retreive changes other users have sent to the remote repo

###git push
Send your changes to the remote repo

There's a lot of terminology, you'll get used to it! I also put together a [glossary](glossary.md) of the terms in this tutorial, which you can refer back to.
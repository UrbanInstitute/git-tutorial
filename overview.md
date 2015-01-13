#An Overview

##What is git?

Git is a piece of software that helps organize and track changes to files over time (usually text based files, like code), and helps multiple users work on the same projects, without stepping on each others' toes. Git is run from the command line (by default the [Terminal](http://en.wikipedia.org/wiki/Terminal_%28OS_X%29) on Macs and the [Command Prompt](http://en.wikipedia.org/wiki/Cmd.exe) on PCs), usually by running `git`, followed by another key word, then often followed by various options.

##What is github?

Github is a website (you're on it now!) that provides a visual interface for git, as well as hosting the files that make up a project. *One* version of these files is hosted on github servers (called the *remote* version), but in almost every case there are many other versions on various other computers. For example, on my computer at work I have a version of these files, and another version on my computer at home. When you follow these tutorials, you'll have your own version(s). As we work on the files, at various times we will sync them up with the remote version that is on github, by **pushing** the changes we make to github and **pulling** down the changes other users make to the remote version.

I go over a few nice github features in [another document](working.md), but most of what we'll talk about is specific to git, not github. Almost all of the functions and commands we talk about are still valid when using services such as [bitbucket](https://bitbucket.org/) or [gitlab](https://about.gitlab.com/).

Many [open-source software projects](http://en.wikipedia.org/wiki/Free_and_open-source_software) are hosted on github (or bitbucket and other git hosting services). Personally, I am a passionate proponent for open-source software, working in the open, and the open data movement. I'd be happy to chat more about the whys and the hows of open-source development, and [many](https://github.com/18F/open-source-policy/blob/master/policy.md) [other](http://www.gnu.org/gnu/manifesto.html) [folks](https://okfn.org/opendata/why-open-data/) have written more eloquently and thorougly than I ever could.

Most software developers write their code using git, sometimes in public, sometimes in private (charging for private hosting is one way github makes money). The more you work with git, the more invaluale it will become to you.

##A glossary of terms

Github has a [similar glossary](https://help.github.com/articles/github-glossary/) online, but here's a stripped down version of just the terms I use in this tutorial

##Git terms

- **branch:** A separate version of a repository, where user(s) can work without making changes to the main branch (called master). Often, after finishing work in a branch, user(s) will *merge* the branch back with master.

- **clone:** The local version of a given repository on a given user's local computer. You can work on a clone from anywhere, even if you're offline.

- **commit:** Instead of saving files, you commit them to git. When you've made changes to one or multiple files, all those changes are stored in one commit (it's a verb and a noun). The commit has a unique id, and is described by a **commit message** which sums up the changes.

- **merge:** In some cases, instead of **pushing** straight to the remote repository, you will **merge** changes into the repository. Sometimes this is because you were working on a separate **branch** that needs to be merged, sometimes this will be because you encounter a **merge conflict**, which is when your changes and changes another user made contradict each other.

- **pull:** When you retrieve the changes made to the remote repository from other clones.

- **push:** When you save the commits made on your local clone to the remote repository.

- **remote:** The version of a repository that is hosted on a server, in our case on Github.com.

##Github terms

- **collaborator:** The people who can directly push to a given repository. At Urban, everyone on this team has been added as a collaborator. Github also makes it possible to push code to projects that you're not a collaborator on (as long as that push is aproved by a collaborator), which is awesome but outside the scope of this tutorial. If you're interested, check out [this article](https://help.github.com/articles/using-pull-requests/) on github.com about contributing to repositories when you're not a collaborator.

- **issue:** A suggestion made on github.com to improve a repository, fix a bug, clarify an explanation, etc. Anyone who can view a repository can open an issue, and the collaborators on that repository moderate the issues (for example, **closing** an issue means it has been solved).

- **repository:** Also called a **repo**. A project on github, made up of multiple files and folders. For example, this repository is called git-tutorial


##Other terms

- **command line flag:** A way to specify certain options when running commands from the Terminal. Often they look like `command_name -x` or `command_name --option` (note single letter flags are preceded by one dash, longer flags by two dashes)

- **environment variable:** A variable, often given a value in your **.bash_profile** file, that can be accessed from any prompt in your Command Line Interface (e.g. the Terminal).

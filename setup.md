# Getting started
**Note: to follow these steps, you'll either need admin rights on your computer or will need some help from Tech&Data to install a few programs.**

## The command line

### Installation

The best way to work with git and github is via the **command line**, a way to interact with your computer using text-only commands, instead of point-and-click. To work with git, you'll need a command line program that let's you use a certain syntax of commands, called "unix". You might also see these programs referred to as "bash" or "bash shells".

On a Mac, the command line can be accessed via the built-in Terminal program, or I prefer the [iTerm2](https://www.iterm2.com/) program which has some added functionality. On a PC, we suggest installing the [ConEmu](https://conemu.github.io/) program which gives you access to a variety of bash shells.

### Basic commands
There's a wide variety of built-in commands you can use on the command line. Then you can install various programs (like `git`!) to add more commands. In these tutorials, you'll be asked to run a variety of commands (both built-in and from `git`), but there are two main commands that will help you navigate the bash environment.

#### cd
Whenever you open a bash shell, each window corresponds to a given location in your file system (just like an Explorer window on a PC or a Finder window on a Mac). The `cd` command stands for "change directory", so it's a way to move between different folders on the command line.

Normally you'd type `cd MyFolderName` then hit enter to move to a different folder (in general, you always hit enter to run a given command). There's also a special command, `cd ..` which moves you one level up in the directory structure (to the parent folder of your current location)

A tip: if you start typing a folder name (e.g. `cd MyFo`) then hit the `tab` key, your bash shell should autocomplete the folder name for you.

#### ls
The `ls` or "list" command lists the files and folders in your current location. It's a good way to get your bearings, and to figure out which folder you need to `cd` into.


## Text Editor

Git processes will sometimes automatically open up a file, which you'll need to edit or save. By default, these files will open in an editor inside the terminal, called [vim](http://www.vim.org/), which is very difficult to use. We're going to override vim, and make these files open in the much friendlier [Sublime](http://www.sublimetext.com/) text editor.

1. Open a Terminal window.
2. Run the command `mkdir ~/bin` which makes a new folder in your home directory called "bin" (mkdir stands for "make directory").
3. Run the following command:
	Sublime Text 2:
	`ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/sublime`
	Sublime Text 3:
	`ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/sublime`.
The `ln` command links two files together (like a shortcut in Windows), in this case you're linking the `subl` program in your Applications folder to a shortcut inside the `bin` folder you just created in step 2.
4. Next you need to open (or create) a file called your `.bash_profile`, which is basically a configuration file for your Terminal. First, run `touch ~/.bash_profile` which will create the file, if it doesn't already exist (the `.` in front of the file name mean's it's a hidden file). Next, run `open ~/.bash_profile` which opens the file (it's probably blank, that's OK).
5. Add a new line to the `.bash_profile` file that says `export PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:~/bin`. `PATH` is called an **environment variable**, which is a variable that represents a value you can access from any Terminal window. The `PATH` environment variable tells your computer where to look for default commands (like `ls`, `mkdir`, `ln`, etc). The new setting in your bash profile updates the `PATH` variable, so that now Terminal will look inside the `~\bin` folder for default commands (along with a number of other folders). Save `.bash_profile` but don't close it yet.
6. Close your Terminal window, and open a new one.
7. Now, the command `sublime` should be a default. Type it into the Terminal and a Sublime Text window should pop up (*A handy aside: you can now open files with Sublime straight from the Terminal. If you're inside a folder and want to open all files and subfolders, for example, type `sublime .` The `.` represents "the folder I'm currently in"*)
8. Finally, you want to set `sublime` as the default editor, instead of vim. In your still-open `.bash_profile` file, add another new line that says `export EDITOR='sublime -w'`, which stores the `sublime -w` command in an environment variable called `EDITOR`. Hooray! (*Another aside: `-w` is called a * *command line flag* *, which allows commands to be run with certain options or settings. `-w` means that the `sublime` command will wait to exit until you close whatever file was opened by the command, which is important for git to work properly*)
9. Close the Terminal window.

## Install git

This one's a lot simpler!

On newer Mac's (OS 10.9 or newer), just try to run `git` from the command line. If it's not installed, a pop-up will prompt you to download XCode Command Line Tools (one of those tools is git). For instructions in other operating systems, including Windows, check out the [tutorial on git's website](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## Get setup with github

1. Make an account at [github.com](https://github.com/).
2. Associate your e-mail address with your github account.
	- You can find a tutorial [here](https://help.github.com/articles/setting-your-email-in-git/), but the only steps you should need are below
	1. Run this command `git-config --global user.email "your_name@urban.org"` with "your_name" replaced with...your name. You could also use your personal e-mail address if you like.
	2. From github.com, add the e-mail address you used to your github account, you can find [instructions here](https://help.github.com/articles/adding-an-email-address-to-your-github-account/).

And you're done!

**Optional:** Down the road, you might find yourself annoyed entering your github username and password in the Terminal when you push code (if you don't know what I'm talking about, you will soon!) If so, there are two solutions, I'll just link to the excellent github tutorials instead of listing the steps:

[Store your username and password in your Mac's keychain](https://help.github.com/articles/caching-your-github-password-in-git/)

or

[Access github via ssh instead of https, and use your ssh key instead of a password](https://help.github.com/articles/generating-ssh-keys/)

### NEXT: [Working with git!](working.md)

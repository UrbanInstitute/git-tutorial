#Getting started

###Text Editor
Git processes while sometimes automatically open up a file, which you'll need to edit. By default, these files will open in an editor inside the terminal, called [vim](http://www.vim.org/) which is very difficult to use. We're going to override vim, and make these files open in the much friendlier [Sublime](http://www.sublimetext.com/) text editor.

1. Open a Terminal window.
2. Run the command `mkdir ~/bin` which makes a new folder in your home directory called "bin" (mkdir stands for "make directory").
3. Run this command `ln -s "/Applications/Sublime Text 2.app/Contents/SharedSupport/bin/subl" ~/bin/sublime`. The `ln` command links two files together (like a shortcut in Windows), in this case you're linking the `subl` program in your Applications folder to a shortcut in the `bin` folder you just created in step 2.
4. Next, run `export PATH=/usr/local/bin:/usr/local/sbin:~/bin:$PATH`. `PATH` is called an *environment variable*, which is a variable which represents a value you can access from any Terminal window. The `PATH` environment variable tells your computer where to look for default commands (like `ls`, `mkdir`, `ln`, etc). The above commands updates the `PATH` variable to look inside the `~\bin` folder made in step 2 for default commands.
5. Now, the command `sublime` should be a default. Type it into the Terminal and a Sublime Text window should pop up.
6. Finally, you want to set `sublime` as the default editor, instead of vim. Run `export EDITOR='sublime -w'`, which stores the `sublime` command in an environment variable called `EDITOR`. Hooray!

###Get setup with github

This one's a lot simpler!

1. Make an account at [github.com](https://github.com/) (which you've probably already done).
2. Associate your e-mail address with your github account.
	- You can find a tutorial [here](https://help.github.com/articles/setting-your-email-in-git/), but the only steps you need should be below
	1. Run this command (slightly modified) `git-config --global user.email "your_name@urban.org"` with "your_name" replaced with...your name. You could also use your personal e-mail address if you like.
	2. Add the e-mail address you used to your github account, you can find [instructions here](https://help.github.com/articles/adding-an-email-address-to-your-github-account/).

And you're done!

3. **Optional:** Down the road, you might find yourself annoyed entering your github username and password in the Terminal when you push code (if you don't know what I'm talking about, you will soon!) If so, there are two solutions, I'll just link to the excellent github tutorials instead of listing the steps:
	1. [Store your username and password in your Mac's keychain](https://help.github.com/articles/caching-your-github-password-in-git/)
	or
	2. [Access githuh via ssh instead of https, and use your ssh key instead of a password](https://help.github.com/articles/generating-ssh-keys/)
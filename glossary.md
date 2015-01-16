###A glossary of terms

Github has a [similar glossary](https://help.github.com/articles/github-glossary/) online, but here's a stripped down version of just the terms I use in this tutorial

###Git terms

- **branch:** A separate version of a repository, where user(s) can work without making changes to the main branch (called master). Often, after finishing work in a branch, user(s) will *merge* the branch back with master.

- **clone:** The local version of a given repository on a given user's local computer. You can work on a clone from anywhere, even if you're offline.

- **commit:** Instead of saving files, you commit them to git. When you've made changes to one or multiple files, all those changes are stored in one commit (it's a verb and a noun). The commit has a unique id, and is described by a **commit message** which sums up the changes.

- **merge:** In some cases, instead of **pushing** straight to the remote repository, you will **merge** changes into the repository. Sometimes this is because you were working on a separate **branch** that needs to be merged, sometimes this will be because you encounter a **merge conflict**, which is when your changes and changes another user made contradict each other.

- **pull:** When you retrieve the changes made to the remote repository from other clones.

- **push:** When you save the commits made on your local clone to the remote repository.

- **remote:** The version of a repository that is hosted on a server, in our case on Github.com.

###Github terms

- **collaborator:** The people who can directly push to a given repository. At Urban, everyone on this team has been added as a collaborator. Github also makes it possible to push code to projects that you're not a collaborator on (as long as that push is aproved by a collaborator), which is awesome but outside the scope of this tutorial. If you're interested, check out [this article](https://help.github.com/articles/using-pull-requests/) on github.com about contributing to repositories when you're not a collaborator.

- **issue:** A suggestion made on github.com to improve a repository, fix a bug, clarify an explanation, etc. Anyone who can view a repository can open an issue, and the collaborators on that repository moderate the issues (for example, **closing** an issue means it has been solved).

- **repository:** Also called a **repo**. A project on github, made up of multiple files and folders. For example, this repository is called git-tutorial


###Other terms

- **command line flag:** A way to specify certain options when running commands from the Terminal. Often they look like `command_name -x` or `command_name --option` (note single letter flags are preceded by one dash, longer flags by two dashes)

- **environment variable:** A variable, often given a value in your **.bash_profile** file, that can be accessed from any prompt in your Command Line Interface (e.g. the Terminal).
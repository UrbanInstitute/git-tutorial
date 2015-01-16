
Sometimes, you might want to work on a separate version of a project, and make lots of frequent commits to the project (as you always should!), but you want the separate version to be isolated from the main version. The different versions of a git project are called **branches**, and the main version is always called the **master** branch. Every project has a master branch by default, but you can create as many new branches as you'd like. At any time, you can **merge** a branch back with master, pushing whatever changes you made in that branch to the master branch as well. You might want to branch a project for a number of reasons:
- Often, if you're working on new feature for a project, you want to be able to work on that new feature without stepping on the toes of other users. Say, for example, you were updating all of the Urban styles to fit a new styleguide. You could make a `new-styleguide` branch, and work on that, but while you were working, other team members could continue pushing to the master branch, without having to use your half-finished wonky styles.
- Down the road, Urban graphics or features might be directly linked to a git repo (i.e. the live version of something on our site could live as a cloned repo on one of our servers). If/when that's the case, the best practice is to **never** push directly to master. Instead, we could push changes to a branch called "staging" or something similar. On a separate server (not the one that hosts the live version), we could have a git repo that is a clone of the staging branch. After internally viewing the staging version, we would then merge the staging branch with the master branch.

Ok, so let's get branching! In the examples below, Urban has just changed leadership, and our new president, Arahsay Artellway, who wants us convert all our documentation to pig latin. I decide to do the translation on a separate branch, so that while I'm working, people can continue to view the master branch without seeing my partway done translations.
1. To create a new branch, called "piglatin" the command is:
```bash
git checkout -b piglatin
```
Next, let github know that you have create a new branch, by running
```bash
git push --set-upstream origin piglatin
```
This is a slightly different use of the "push" command from above, since you're not pushing changed files, you're pushing the fact that a new branch exists. The `--set-upstream` flag means that now, every time you type `git push` as you're working in the piglatin branch on your computer, the changes get pushed to the piglatin branch on github.

2. Now, you can work on the branch. In this example, I [painstakingly translated](http://www.snowcrest.net/donnelly/piglatin.html) all these markdown files into piglatin. At first, these kind of changes might feel weird or alarming. It feels like you're deleting all your hard work! But remember, the two different branches store two entirely differnt versions of the repo. While you make changes in `piglatin`, the `master` branch stays the same.

3. On a branch, the git workflow is exactly the same as described above. As you change files, `add`, `commit`, `pull`, and `push`.

4. If you want to switch branches, you use the `checkout` command again, but without the `-b` flag (b stands for "branch" and is just used to create a *new* branch). It's <strong><span style="color: red">important to remember</span></strong> to commit and push your changes before switching to another branch. In some cases (and it's a bit complex to go into the specifics of which cases), not commiting and pushing can make you lose local changes (i.e. changes you've made on your own computer, but haven't yet synced up with github), when switching between branches. Once you've committed and pushed, run
```bash
git checkout piglatin
```
to switch to the piglatin branch, or
```bash
git checkout master
```
to switch back to the main branch.

5. Sometimes, you will want to combine two branches together. There are two variations on why and when you'd do this:

####Merging from master into a branch

Sometimes, you'll want to keep working on a new branch, but also pull in changes that other users have made to the master branch. Using the example from above, say you're on a branch called `new-styleguide`, where you're doing some major Urban CSS updates. As you're working, folks have been building a new feature over on the `master` branch. You want to pull that new feature into your branch, so you can see how your new styles fit with it.

1. Make sure you're on the `new-styleguide` branch, or switch to it with
```bash
git checkout new-styleguide
```

2. Run
```bash
git pull origin master
```
This pulls changes *from* master *into* new-styleguide.

3. This is called **merging** the two branches, and you might need to resolve differences that contradict each other (see below for this process).

####Merging a branch into master
So you've finished all your work updating the new styleguide on your branch. High five! If you want to update the master branch with all your changes, the process is just the reverse of above:
1. Make sure you're on the `master` branch
```bash
git checkout master
```

2. Then pull in your changes
```bash
git pull new-styleguide
```

###Deleting a branch
Finally, there are times you might want to delete a branch. Major branches, like `new-styleguide` or other big features, might be good to keep around. Lots of software products have branches for each new version (1.0, 2.0 etc), and looking back at those branches can often be helpful, to help diagnose bugs, or even let users roll back to old versions of the software. But little branches, for small fixes or updates, can sometimes be deleted. To delete a branch:
1. Switch to a branch other than the one you want to delete using `git checkout`

2. Running
```bash
git branch
```
will show you a list of all the branches on the project.

3. Then, to delete a branch called `temporary-stuff`, for example
```bash
git branch -D `temporary-stuff`
```

##Resolving a merge conflict

















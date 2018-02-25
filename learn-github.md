# How to use GitHub locally

First, the reason we are using GitHub is because it makes it so much easier to work in teams! It minimizes the chance that any one change breaks the project. It also allows you to see what other people
have been working on. There's a bit of a learning curve but you really only need to learn a few commands to be successful.

### Install `git`

* [Mac](https://desktop.github.com/)
* [Windows](https://desktop.github.com/)
* Linux
  * `$ sudo dnf install git-all`
  * Didn't work? Try `$ sudo apt-get install git-all`

### Terminology

* `Repository` is like a folder! It collects all of your work for a specific project.
* `Clone`ing a repository is like copying it.
* `Pull requests` are a way to `merge` your changes into a `repository`
* You can also `pull` changes into your branch before you `merge` to prevent some error messages
* You can `commit` local changes and then `push` them to your branch on GitHub

### Cheat sheet

* [cheat sheet 1](https://education.github.com/git-cheat-sheet-education.pdf)
* [cheat sheet 2](https://gist.github.com/davfre/8313299)

### How to copy a repository to your local folders

1. Navigate to the folder you want from github. For example, if you wanted to work with the `mac-share` repository, you would go [here](https://github.com/mac-ds-4-good/mac-share).

2. Your screen should look like this!

![mac share home screen](/images/github_top.JPG)

3. To get all of the files, you'll need to `clone` the repository (copy the repository). Click the green `Clone or download` button in the right-hand corner.

4. Click the `copy to clipboard` icon (or just copy the url).

5. Navigate to your terminal (Mac) or command prompt (PC)

6. Choose where you want to put this file. On my PC, to save it in my Documents folder, I type `cd Documents`.

7. Type `git clone {url}`, but replace `{url}` with what you just copied.

8. Congrats! Now you can edit the files on your computer.

### Push local changes to GitHub

1. In your command prompt/terminal, navigate to the correct folder. If you're on a Mac you can see where you are if you type `pwd` (personal working directory). The PC equivalent is `cd` (current directory).

2. Type `git remote add origin {url}.git`. Replace {url} with the repository url from your internet browser.

3. Now you need to add your own branch! The `master` branch should only be where we put our polished work, to keep things clean. To make your own branch, type `git checkout -b {name}`. I recommend using your first name as the name of your branch.

4. If you're ready to `push` your changes, type  `git status` to check which files you're about to move. It's good to spot check just in case something is included that you didn't mean to have.

5. If everything looks good and you want to commit all the files, type `git add .` to add everything, then type `git commit -m "{message}"`, replace {message} with a quick description of what you're pushing.  

6. To push everything (last step!), type `git push -u origin {your branch}` (in the future you should be able to just type `git push`). At first it will say "fatal HttpRequestException encountered." Really, it's just prompting you for your username and password to make sure you actually have write access to the repository. 

7. If you get an error saying something along the lines of your branch is behind, try typing `git pull` to merge any remote changes you may have made.

### A few notes

**Please** do not change anyone else's working branch! It can cause problems and is a pain to fix sometimes.

For now I'll be only person who merges pull requests to the master branch while everyone gets used to GitHub. If you want to submit your pull request (merge your branch with the master branch), let me know! I'll give you more detailed instructions.

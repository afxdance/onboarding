# How to: Use Git branches and GitHub pull requests

| Note for VM users (ie. Windows)  |
| :------------------------------- |
| You can do all of these steps either inside or outside the VM. If you do it outside the VM, use [Git Bash](https://git-for-windows.github.io/) and make sure SSH keys are set up ([instructions](set-up-github-account.md)) outside the VM as well. |


Git is a way to keep backups and track changes in a code project.

Git has two basic concepts:

 - **Commits.** A commit is a snapshot all the files in the repository at a particular time.
 - **Branches.** A branch is a pointer or link a particular line of commit history.

You might be used to making copies of an essay (`essay.docx`, `essay-final.docx`, `essay-finalfinal.docx`), or perhaps you've made copies of a folder of code, to keep track of old versions. If you use Git, here's what that might look like:

![screen shot 2017-10-29 at 2 21 10 pm](https://user-images.githubusercontent.com/1570168/32148455-8e95fff4-bcb4-11e7-8625-5b7692575a35.png)

Each of those dots is a commit, or a version of all your files. The dots are connected to show the progression of your history. 

When you want to add your own work, first make a **branch**.

**How to make a branch**

 1. Only if you want to re-use a branch you've made before: You need to delete it first.\
    `git branch -d your_branch_name`\
    If you do have unmerged work in the branch, don't delete it, just make a new branch with another name.
 2. Start by making sure you're on the `master` branch.\
    `git checkout master`
 3. Make sure `master` is up to date.\
    `git pull`
 4. Branch off `master`.\
    `git branch your_branch_name`\
    You can technically name your your branch anything, but you should include your GitHub username in it, so that other people will know who is responsible for it. Examples: `git branch szhu` or `git branch szhu-refactor`
 5. Switch to being on the `your_branch_name` branch.\
    `git checkout your_branch_name`

Great, now you're on your own branch!

Now you can make changes to the code. Whenever you want to save a version of your code, you need to make a commit.

**How to make a commit**

 1. See which files you've changed.\
    `git status`
 2. Read this: When you make a commit, you first tell Git which changed files to add to the commit (using `git add`), then you actual make the commit (using `git commit`). The files you've `git add`ed is called the **stage** or **index**.
 3. Stage the files whose changes you want to include in the commit.\
    `git add path/to/file`\
    Do this for each applicable file.
 4. Now you can make the commit.\
    `git commit`
 5. Read this: Now you're in a window where you can type a commit message. A commit message looks like this:
    ```
    A short title, which briefly describes your changes
    
    Optionally additional info in the lines below if the commit is complex.
    For example, you can describe the bug you fixed or the feature you made.
    ```
 6. How to write a good commit title:
     - Use present tense, capitalize, no period at the end.
     - Example: Refactor app/models/user.rb
     - Example: Add team switch/drop functionality
     - Example: Make code pass style guide
 6. Type your commit message, save, and close.
     - If the window is inside the terminal: You're inside a program called Vim. Press `a`, type your commit message, press Escape, then type `:wq`.
     - If the window is a Sublime Text window, just type your commit message, save, and close the tab.

The terminal should now show that the commit is made! Your commit graph now looks like this:

![screen shot 2017-10-29 at 3 13 40 pm](https://user-images.githubusercontent.com/1570168/32149016-c42173cc-bcbb-11e7-8890-74fba52223f1.png)

Everything we've done up to now is all happening offline. If you want your branch to show up on github.com, you need to push your branch.

**How to push your current branch**

 1. This will make `git push` do what you expect:\
    `git config push.default current`\
    You only have to do this once for each repo you clone.
 2. Push!\
    `git push`

If you want your changes to be on the `master` branch, you need to merge your branch into `master`.

**How to merge your branch into master using GitHub**

 1. Switch to your branch: `git checkout your_branch_name`
 2. Push the branch, following the guide above.
 3. Go to the repository on github.com.
 4. There is a button that looks like this:\
    ![screen shot 2017-10-29 at 3 27 33 pm](https://user-images.githubusercontent.com/1570168/32149172-b3afac96-bcbd-11e7-93a1-c7397315390d.png)\
    Click it and switch to your branch.
 5. Click Compare and Pull Request.\
    If you don't see that button, maybe you haven't made any commits on the branch, or maybe you didn't push your branch after you made the commits.
 6. Make sure the title of the pull request is okay, then click Create pull request.
 7. Now you should see the pull request! If it says that "a review is required", have someone else take a look at the pull request and click the "Add your review" button to approve the pull request.
 8. Either you or the review and click "Merge pull request" to merge it into `master`!


**What do do when you're done with your branch and pull request**

 1. On GitHub, delete the branch. (optional, because we can always mass delete them)
 2. On your computer: `git checkout master`
 3. On your computer: `git pull`
 

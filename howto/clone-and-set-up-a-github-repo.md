# How to: Clone and set up a GitHub repo

Code on GitHub is broken down into projects called repositories (repos). To download a syncable copy of the a repo, you need to clone it.

| Note for VM users (ie. Windows)                                                    |
| :--------------------------------------------------------------------------------- |
| You need to be `vagrant ssh`d in. All commands below need to be run inside the VM. |


### cd into afxdance folder

 1. `cd ~/afxdance`


### Clone repo from GitHub

 1. You're reading this page because you want to clone and set up a specific GitHub repo. The repo you want to clone is probably located at the webpage that sent you here. Go visit the repo on github.com now.
 2. Click the green "Clone or Download" button.
 3. Make sure SSH is selected.
 4. Copy the SSH URL.
 5. Then clone the repo into the afxdance folder as follows:\
    `git clone PASTE_YOUR_URL_HERE`
 6. `cd` into the repo you just cloned.


### git config user.name and user.email

Git needs to know who you are when you make commits.

 1. `git config user.name "Your Real Name Here"`
 2. `git config user.email "youremailhere@example.com"`\
    Use the same email you set as your primary email in https://github.com/settings/emails above.


### Open the entire repo in Sublime

 1. If you're not in a VM:\
    `subl .`
 2. If you're inside a VM:\
    Open Sublime Text, go to File > Open Folder, then open the repo you cloned.


### You're done!

You've cloned the repo and configured Git correctly.

Now go back to the repo's own page to see additional instructions.

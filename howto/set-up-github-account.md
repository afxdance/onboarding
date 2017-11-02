# How to: Set up GitHub account


### Make sure your GitHub account is set up properly

**Why we need this**\
GitHub has a feature where you can edit files directly from the web at github.com. We need to when you make commits this way, these web commits are correctly attributed to you.

**How to set up**

 1. Go to https://github.com/.
 2. Make sure you're logged in, or make an account if you need to.
 3. Go to https://github.com/settings/profile.\
    Make sure your real name is set correctly.
 4. Go to https://github.com/settings/emails.\
    Make sure the primary email is the one you want to have associated with you (possibly publicly) when you make commits. If you're not sure which email to use, most people use their Berkeley email.


### Get access to the afxdance org

**How to set up**

 1. If you're not added to the afxdance GitHub organization yet, ask your mentor or project lead to add you. Give them your GitHub username.


### SSH keys

**Why we need this**\
SSH keys let sites like GitHub know who you are -- it tells GitHub that you're logged in as you when you git clone/push/pull. The key has two files -- a **private key** that should never be shared, and a **public key** that you should share with websites (like GitHub) that you want to use it with.


**How to set up** (adapted from [here](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) and [here](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/))

 1. Make a SSH key for your computer as follows:\
    `ssh-keygen`
 2. Press Enter at each prompt (this uses the default options).
 3. If you get a message that the file already exists, then you've already made a key before. Ctrl-C to exit the wizard, but don't skip any steps below.
 4. Open the public key as follows:\
    `subl ~/.ssh/id_rsa.pub` OR `cat ~/.ssh/id_rsa.pub`
 5. Copy all the contents of the file.
 6. Go to https://github.com/settings/keys.
 7. Click New SSH key. Fill it out as follows:
     - Title: (leave empty)
	 - Key: (paste contents of `~/.ssh/id_rsa.pub` in this box)


### Some fun (entirely optional) things you might want to set up

 1. Add a profile picture! You can upload one either
      - on GitHub: https://github.com/settings/profile
      - or on Gravatar: https://en.gravatar.com \
        Make sure you add the email you use with GitHub to Gravatar, and your profile picture should update in a few minutes.

 2. Your profile shows the organizations you are in:\
    ![screen shot](https://user-images.githubusercontent.com/1570168/32304380-fb4e96e6-bf2b-11e7-9719-9d85392ee548.png)\
    But, by default, this is only visible to other people in the same org. If you want this visible publicly, go here:\
    github.com/orgs/afxdance/people?query=YOUR_USERNAME_HERE \
    and change "Private" to "Public".\
    (Instructions adapted from [here](https://help.github.com/articles/publicizing-or-hiding-organization-membership/).)

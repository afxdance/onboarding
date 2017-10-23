Please read all of these instructions carefully. If you're sure if you've already done a step before, just do it again.


### Install developer tools
You might need to install some tools that will let you install the tools below. Open a terminal window and type:

```shell
clang
```

You should get a prompt to install some software. If not, don't worry, it's probably installed already.


### Install Homebrew
Homebrew is a package manager. It lets you install software just by typing a command into the terminal. Install Hombrew as follows:

```shell
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
(Taken from the instructions at https://brew.sh/.)

Say yes to the on-screen prompts. Note that when you type your password into the terminal, you won't see any feedback -- just type it and press Enter.

**If you already have Homebrew installed, run the following to update it:**

```shell
brew update
```


### Install RVM (Recommended)
RVM allows you to install and manage Ruby environments.

Windows:
```shell
gpg--keyserverhkp://keys.gnupg.net--recv-keys409B6B1796C275462A1703113804BB82D39DC0E37D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable
```
(Taken from the instructions at https://rvm.io/)

Mac:
```shell
\curl -sSL https://get.rvm.io | bash -s stable
```
(Taken from the instructions at https://rvm.io/)


### Install PostgreSQL
PostgreSQL (or Postgres) is a kind of database. You won't be using PostgreSQL on your computer, but Rails requires it to be installed. Install Postgres as follows:

```shell
brew install postgres
```


### Install Sublime Text 3 (Recommended)
Sublime Text is an editor. We will only be supporting Sublime Text 3 installed via Homebrew, so please install it exactly as follows:

```shell
brew cask install sublime-text --force
```

- Please do this even if you are already using Sublime Text 2. Sublime Text 2 may not support all the plugins we will be using.
- Please do this even if you are already using Sublime Text 3 installed not via Homebrew. Installing via Homebrew gives you the `subl` command-line command, which we will be using below.



### Set Sublime as the default command-line text editor (Recommended)
This sets Sublime text to be your default editor when command-line apps like Git request it. If you don't set it, Git commands might drop you into Vim, which has special instructions for using it. For example, to just exit Vim, you need to type `:q`.

Open your Bash config file as follows:

```shell
subl ~/.bash_profile
```

Then add these lines to the bottom and save:
```bash
export EDITOR='subl --wait'
export GIT_EDITOR='subl --wait'
```


### Set up directory structure (Recommended)
It would be convenient to 

Create a folder in your on your computer for afx code at ~/afxdance


### SSH keys (recommended)

SSH keys help sites like GitHub know who you are -- it's kind of telling GitHub that you're logged in as you. You need to make a SSH key for your computer as follows:

```shell
ssh-keygen
```

This starts a wizard that walks you through various options. You can use the defaults at each prompt by just pressing Enter.

The key has two parts -- a private key that should never be shared, and a public key that you should share with websites you want to use it with. Open the public key as follows, and copy all the contents of the file:

```bash
subl ~/.ssh/id_rsa.pub
```

Go to https://github.com/settings/keys and click New SSH key.

You can leave the title empty. Paste the contents of `~/.ssh/id_rsa.pub` into the Key box.

(Taken from instructions at https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/ and https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/.)


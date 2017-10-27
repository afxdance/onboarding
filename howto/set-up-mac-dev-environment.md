# How to: Set up your Mac dev environment


### Xcode developer tools

**Why we need this**\
Some of the software below requires a C compiler. This is the easiest way to install a C compiler on Mac.

**How to install**

 1. `cc`
 2. You should get a pop-up dialog to install some software. If not, don't worry, it's probably installed already.


### Homebrew (`brew`)

**Why we need this**\
Homebrew is a command-line tool that makes it easier to install some of the software below.

**How to install** (adapted from https://brew.sh/)

 1. `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
 2. Say yes to the on-screen prompts.
 3. When you need to enter your password, note that you won't see any feedback when you type. Just type it and press Enter.

**If you already have Homebrew installed, run the following to update it**

 1. `brew update`


### RVM

**Why we need this**\
We have projects that require a specific version of Ruby. RVM makes it easy to install specific versions of Ruby.

**How to install** (adapted from https://rvm.io/)

 1. `\curl -sSL https://get.rvm.io | bash -s stable`


### PostgreSQL

**Why we need this**\
PostgreSQL (or Postgres) is a kind of database. Rails requires it to be installed.

**How to install**

 1. `brew install postgres`


### Sublime Text 3 (`subl`)

**Why we need this**\
Sublime Text 3 is a code editor. We specifically want you to install Sublime Text 3 (not Sublime Text 2), because it is compatible with more plugins. Installing via Homebrew gives you the `subl` command-line command, which we will be using below.

**How to install**

 1. `brew cask install sublime-text --force`



### Set Sublime as the default command-line editor

**Why we need this**\
This will make it easier to, among other things, make Git commits. For example, when you type `git commit`, Sublime will open instead of Vim.

**How to set up**

 1. Open your Bash config file as follows:\
    `subl ~/.bash_profile`
 2. Add these lines to the bottom:
    ```bash
    export EDITOR='subl --wait'
    export GIT_EDITOR='subl --wait'
    ```
 3. Save!
 4. Restart your shell to load these new settings:
    `exec bash -l`


### Set up directory structure

**Why we need this**\
In the following setup instructions, we will assume that you have a folder located at `~/afxdance` where all your cloned repos will be.

**How to set up**

 1. `mkdir -p ~/afxdance`

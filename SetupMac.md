Please read all of these instructions carefully. If you're sure if you've already done a step before, just do it again.


### Install developer tools

Some of the software you need below requires a C compiler to be installed. Install a C compiler and related tools as follows:

```shell
cc
```

You should get a pop-up dialog to install some software. If not, don't worry, it's probably installed already.


### Install Homebrew

Homebrew is a package manager. It makes it easier to install the software you need below. Install Hombrew as follows:

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

RVM makes it easy to install a specific version of Ruby, which we need. Install RVM as follows:

Windows:

```shell
gpg--keyserverhkp://keys.gnupg.net--recv-keys409B6B1796C275462A1703113804BB82D39DC0E37D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable
```

Mac:

```shell
\curl -sSL https://get.rvm.io | bash -s stable
```

(Taken from the instructions at https://rvm.io/.)


### Install PostgreSQL

PostgreSQL (or Postgres) is a kind of database. You won't be using PostgreSQL on your computer, but Rails requires it to be installed. Install Postgres as follows:

```shell
brew install postgres
```


### Install Sublime Text 3 (Recommended)

Sublime Text 3 is a code editor. **Please install it exactly as follows:**

```shell
brew cask install sublime-text --force
```

**We will only be supporting Sublime Text 3 installed via Homebrew.**

- Please follow the above instructions even if you are already using Sublime Text 2. Sublime Text 2 may not support all the plugins we will be using.
- Please follow the above instructions even if you are already using Sublime Text 3 installed not via Homebrew. Installing via Homebrew gives you the `subl` command-line command, which we will be using below.


### Set Sublime as the default command-line text editor (Recommended)

This will make it easier to, among other things, make Git commits.

(Details: This sets Sublime text to be your default editor for command-line apps like Git. If you don't set it, `git commit` may drop you into Vim, which does not behave like other command-line apps. For example, to just exit Vim, you need to type `:q`.)


Open your Bash config file as follows:

```shell
subl ~/.bash_profile
```

Then add these lines to the bottom and save:

```bash
export EDITOR='subl --wait'
export GIT_EDITOR='subl --wait'
```


Restart your shell to load these new settings:

```
exec bash -l
```


### Set up directory structure (Recommended)

In the following setup instructions, we will assume that you have a folder located at `~/afxdance` where all your cloned repos will be. Create this folder now if you haven't already:

```shell
mkdir -p ~/afxdance
```


### SSH keys (Recommended)

SSH keys help sites like GitHub know who you are -- it tells GitHub that you're logged in as you when you git clone/push/pull. You need to make a SSH key for your computer as follows:

```shell
ssh-keygen
```

This starts a wizard that walks you through various options. You can use the defaults at each prompt by just pressing Enter.

If you get a message that the file already exists, then you've already made a key before. Ctrl-C to exit the wizard, but continue to follow the instructions in the next paragraph.

The key has two parts -- a private key that should never be shared, and a public key that you should share with websites you want to use it with. Open the public key as follows, and copy all the contents of the file:

```bash
subl ~/.ssh/id_rsa.pub
```

Go to https://github.com/settings/keys and click New SSH key.

You can leave the title empty. Paste the contents of `~/.ssh/id_rsa.pub` into the Key box and save.

(Taken from instructions at https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/ and https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/.)

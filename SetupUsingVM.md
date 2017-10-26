Please read all of these instructions carefully. If you're sure if you've already done a step before, just do it again.

### Install VirtualBox and Vagrant

Due to software incompatibilites, we'd like you to set up an Ubuntu virtual machine (VM) rather than running directly on Windows. Don't worry -- the setup is pretty easy and you can actually edit files and use Rails apps outside the VM.

These two tools will help us set up a VM.

As of October 2017, you must install VirtualBox 5.1, not the most recent version 5.2. Here's the link where you can download VirtualBox 5.1:
https://www.virtualbox.org/wiki/Download_Old_Builds_5_1

You can download Vagrant here:
https://www.vagrantup.com/downloads.html

Install both software with all the default options.


### Install Sublime Text 3 (Recommended)

Sublime Text 3 is a code editor. Please install it:
https://www.sublimetext.com/3


### Install Git

Install Git for your operating system:
https://git-scm.com/download


### Set up directory structure (Recommended)

In the following setup instructions, we will assume that you have a folder called `afxdance` where your cloned repos will be. Create this folder now if you haven't already.


### Use the onboarding repo to set up the VM

Open a terminal and cd to the `afxdance` folder.

Then, clone this onboarding repo:

```shell
git clone https://github.com/afxdance/onboarding
```

Now cd into the onboarding repo and start the virtual machine (VM) as follows:

```shell
cd onboarding

# This starts the VM. Do this every time you restart your computer.
vagrant up

# This SSH's into the VM. Do this every time you open a new terminal.
vagrant ssh
```

**Important note!**
Because Vagrant looks for a `Vagrantfile` in the current directory, Vagrant commands need to be run in the `onboarding` repo.

Congratulations! You've made an Ubuntu virtual machine that is running inside your actual machine, and you're now at the terminal prompt for the VM. Everything you type here and software you install here runs inside Ubuntu.


### SSH keys (Recommended)

If you aren't already, make sure you're SSH'd into the VM:

```shell
vagrant ssh
```


SSH keys help sites like GitHub know who you are -- it tells GitHub that you're logged in as you when you git clone/push/pull. You need to make a SSH key for your computer as follows:

```shell
ssh-keygen
```

This starts a wizard that walks you through various options. You can use the defaults at each prompt by just pressing Enter.

If you get a message that the file already exists, then you've already made a key before. Ctrl-C to exit the wizard, but continue to follow the instructions in the next paragraph.

The key has two parts -- a private key that should never be shared, and a public key that you should share with websites you want to use it with. Open the public key as follows, and copy all the contents of the file:

```bash
cat ~/.ssh/id_rsa.pub
```

Go to https://github.com/settings/keys and click New SSH key.

You can leave the title empty. Paste the contents of `~/.ssh/id_rsa.pub` into the Key box and save.

(Taken from instructions at https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/ and https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/.)

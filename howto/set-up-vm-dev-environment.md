# How to: Set up your VM dev environment


### VirtualBox and Vagrant

**Why we need this**\
Your computer cannot directly run our code, so we need to set up a virtual machine (VM), which is a simulated computer running in an app in your actual computer. The VM will be running Ubuntu. VirtualBox and Vagrant are two tools will help us set up a VM.

**How to install**

 1. As of October 2017, you must install VirtualBox 5.1, not the most recent version 5.2. Here's the link where you can download VirtualBox 5.1:\
    https://www.virtualbox.org/wiki/Download_Old_Builds_5_1
 2. Download Vagrant here:\
    https://www.vagrantup.com/downloads.html
 3. Install both software with all the default options.


### Install Sublime Text 3

**Why we need this**\
Sublime Text 3 is a code editor.

**How to install**

 1. Download and install from here: https://www.sublimetext.com/3


### Git

**How to install**

 1. Download and install from here: https://git-scm.com/download


### Set up directory structure

**Why we need this**\
In the following setup instructions, we will assume that you have a folder called `afxdance` where your cloned repos will be.

**How to set up**

 1. Make a folder called `afxdance` and `cd` into it.



### Set up the VM

**How to set up**

 1. `cd` to the `afxdance` folder.
 2. Clone the **onboarding** repo:\
    `git clone https://github.com/afxdance/onboarding`
 3. `cd onboarding`
 4. Start the virtual machine (VM) as follows:\
    ```shell
    cd onboarding

    # This starts the VM. Do this every time you restart your computer.
    vagrant up

    # This SSH's into the VM. Do this every time you open a new terminal.
    vagrant ssh
    ```

**Important note!**\
Because Vagrant looks for a `Vagrantfile` in the current directory, all `vagrant` commands need to be run in the `onboarding` repo.


### You're done!

Congratulations!

 - You've made an Ubuntu virtual machine that is running inside your actual machine.
 - You're now at the terminal prompt for the VM. Everything you type here and software you install here runs inside Ubuntu.

# How to: Set up Atom


Atom is a text editor. It works and looks very similar to Sublime, but it has a few special features, which we'll introduce here as well.

**How to install Atom and the Atom packages we will be using**

 1. Install Atom. Mac users, `brew cask install atom`. Everyone else can go to https://atom.io/ to download the app.
 2. Open your terminal. Windows users, use Git Bash or Command Prompt. Do not use `vagrant ssh`.
 3. We will install a few Atom packages (plugins) using the Atom package manager (apm) as follows:\
    `apm install auto-update-packages blame busy-signal git-plus intentions linter linter-rubocop markdown-preview-opener markdown-preview-plus open-terminal-here pdf-view sort-lines teletype`\
    By the way, you can also install packages using Atom > Preferences > Install, but this is faster for installing a bunch at once.
  4. If Atom asks you whether you want to install dependencies, say yes.
  5. Open the project you want to edit (auditions-app, history-app, etc) in Atom the same way you do in Sublime. You can also take the folder in Finder/Explorer and drag it into an Atom window.


**How to use Atom teletype**

Teletype is an Atom package that lets you share your Atom to let other people type on it. It's like Google Docs for code or Cloud9, except that all changes are saved on the sharer's computer.

 1. Click the teletype icon in Atom's status (bottom) bar. It looks like a tower.
 2. Follow the setup instructions to login with your GitHub account.
 3. One person should be the sharer. Click the teletype icon and click Share. Send your share code to everyone else.
 4. Everyone else, get the share code from the sharer. Click the teletype icon and paste your code in.

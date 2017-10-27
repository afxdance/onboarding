You're here because you want to clone a repo. You can just `git clone` it, but there are a few other steps involved before and afterwards. Please read all the steps here carefully to clone your repo and set it up.


### Get GitHub push access to the afxdance org

You only need to do this once ever.

Go to https://github.com/ and make sure you're logged in. Make an account if you need to.

Go to https://github.com/settings/profile. Please make sure you have your real name set.

Go to https://github.com/settings/emails. Make sure the primary email is the one you want to have associated with you (possibly publicly) when you make commits. If you're not sure which email to use, most people use their Berkeley email.

If you're not added to the afxdance GitHub organization yet, ask your mentor or project lead to add you. Give them your GitHub username.


---

Only if you're using a VM, ie. on Windows: For all the follwing steps, you need to be running commands inside the VM. Make sure you're `vagrant ssh`d in.


### cd into afxdance folder

cd into wherever you created the afxdance directory:

```shell
cd ~/afxdance
```


### Clone repo from GitHub

 1. Go the repo on the GitHub website that you want to clone.
 2. Click the green "Clone or Download" button.
 3. Make sure SSH is selected.
 4. Copy the SSH URL.

Then clone the repo into the afxdance folder as follows:

```shell
git clone PASTE_YOUR_URL_HERE
```

Then cd into the repo. If you cloned afxdance/auditions-app, then you need to `cd auditions-app`.


### git config user.name and user.email

Git needs to know who you are when you make commits. Set your Git identity as follows:

```shell
git config user.name "Your Real Name Here"
git config user.email "youremailhere@example.com"
```

Use the same email you set as your primary email in https://github.com/settings/emails above.


### Open the entire repo in Sublime

```shell
subl .
```


### Rails projects: Install Ruby

When you cd'd into the repo, you might have gotten a warning along the lines of:

```
Required ruby-2.2.2 is not installed.
To install do: 'rvm install "ruby-2.2.2"'
```

If this is the case, follow the printed instructions to install Ruby.


### Rails projects: Install and use Bundler

The repo  contains a file named `Gemfile` that lists the Ruby packages ("Rubygems") that it depends on. Ruby itself doesn't know how to read the `Gemfile` -- you need to install a tool called Bundler as follows:

```shell
gem install bundler
```

The you need to run Bundler itself to install the dependencies in the Gemfile:

```shell
bundle
```


### You're done!

You've cloned the repo, configured Git correctly, and installed the repo's dependencies.

Now go back to the repo's own README file to see more specific instructions.

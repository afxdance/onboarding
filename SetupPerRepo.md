These are the instructions you need to follow for each GitHub repository you want to clone.


### Get GitHub push access to the afxdance org

Go to https://github.com/ and make sure you're logged in. Make an account if you need to.

Go to https://github.com/settings/profile. Please make sure you have your real name set.

Go to https://github.com/settings/emails. Make sure the primary email is the one you want to have associated with you (possibly publicly) when you make commits. If you're not sure which email to use, most people use their Berkeley email.

If you're not added to the afxdance GitHub organization yet, ask your mentor or project lead to add you. Give them your GitHub username.


### cd into afxdance folder

cd into wherever you created the afxdance directory:

```shell
cd ~/afxdance
```


### Clone repo from GitHub

Go the repo on the GitHub website that you want to clone.

Click the green "Clone or Download" button. Make sure SSH is selected, then copy the SSH URL. Then clone the repo into the afxdance folder as follows:

```shell
git clone PASTE_YOUR_URL_HERE
```

Then cd into the repo. If you cloned afxdance/auditions-app, then you need to `cd auditions-app`.


### git config user.name and user.email

Git needs to know who you are when you make commits. Set your Git identity as follows:

```shell
git config user.name "Your Name Here"
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

Ruby projects typically contain a Gemfile that lists the Ruby gems (packages) that it depends on. After these gems are installed, they can be `require`d by Ruby code. Bundler is a tool that can read the Gemfile and install the listed gems. Install Bundler as follows:

```shell
gem install bundler
```

The you need to run Bundler itself:

```shell
bundle
```

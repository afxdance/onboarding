# How to: Set up RuboCop


**About RuboCop and style errors**

 - RuboCop is a style checker for Ruby files.
 - Following a style guide is like writing with proper grammar. It's not strictly required, but it helps readability if all published/submitted work follows the same style.
 - In addition, some style guidelines help you write code that is less likely to have errors, or makes it easier to spot potential errors.
 - RuboCop's default style guide is very strict. If you see a style rule that you think is ridiculous, bring it up with your project lead or mentor. We can turn off unhelpful style rules using a config file in the repo.
 - We want everyone to have RuboCop installed as follows so that you get warnings and errors as you type!


**How to set up**

 1. Windows users only: Follow all the steps on this page **outside** your VM.\
    First, install Ruby directly on Windows. Use this link and install the most recent version: https://rubyinstaller.org/
 2. Make sure you are `cd`d into the repo that you want to use RuboCop on.
 3. `gem install rubocop`
 4. Open Sublime Text.
 5. Read this: Use ⇧⌘P (Mac) or Ctrl+Shift+P (Windows) to open the Sublime Command Palette.
 6. Open the Command Palette and select "Install Package Control".\
    If you don't see that option, don't worry, it's probably already installed.
 7. Open the Command Palette and select "Install Package". Install the "SublimeLinter" package.
 8. Open the Command Palette and select "Install Package". Install the "SublimeLinter-rubocop" package.
 9. Quit Sublime Text (not just close the window, but like Sublime Text > Quit or File > Exit), and open it again.


**How to check if Sublime Text/RuboCop integration is working**

 1. Go to any Ruby file. The `Gemfile` is a Ruby file, as is any file ending in `.rb`.
 2. To quickly search for files in a repo, press ⌘T (Mac) or Ctrl+P (Windows). Then type `Gemfile` or `.rb` and use the arrow keys to go through files. Press Enter to select a file.
 3. Wait a few seconds. If there are yellow marks that appear, then everything is working!
 4. The yellow marks are style guide violations. To see what's wrong, click one of the yellow things, and look at the status bar.
 5. The yellow circles in the gutter (near the line numbers) indicate that the line contains a warning. This can be helpful when you're quickly scrolling through lines.


How to log in, so you can edit pages using this tool:

1. Go to here: <https://github.com/settings/tokens>
2. Click **Generate New Token**
3. Fill out as follows:
    -  Name: "afxdance/onboarding editor" or any name you want
    - Scopes: "repo" and "user:email"
4. Click **Generate token**.
5. Copy the token.
6. Go back to this page.
7. <input type="button" onClick="var result = prompt('Paste the token here:'); result != null && (localStorage['szhu.qa.login'] = result);" value="Click me!" />
8. Then refresh the page!


How to log out:

1. Click the "Click me!" button above
2. Don't enter anything and press OK.
3. Refresh the page.

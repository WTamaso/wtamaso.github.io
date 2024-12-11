---
categories: Git DevTools
---

# Git
--TODO

## Setup
--TODO

### Windows
--TODO

### Linux
--TODO

## Setting Git Username and Email

When using Git, it is essential to configure your username and email address. This information is associated with every commit you make, helping to identify the author of the changes. You can set these configurations globally for all repositories or locally for a specific repository.

### Setting Global Git Username and Email

To set your global Git username and email address, use the following commands:

``` cmd
git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
```
These commands will save the values in the global configuration file (`~/.gitconfig`). You can verify the settings by running:

``` cmd
git config --list
```
This should display your username and email address:

```
user.name=Your Name  
user.email=youremail@yourdomain.com
```

### Setting Git Username and Email for a Single Repository

If you need to use a different username or email address for a specific repository, navigate to the repository directory and run the following commands without the `--global` option:

``` cmd
cd /path/to/your/repository
git config user.name "Your Name"
git config user.email "youremail@yourdomain.com"
```
To verify the repository-specific settings, use:

``` cmd
git config --list
```
This will show the username and email address configured for that particular repository.

### Important Considerations

Global vs. Local Configuration: The global configuration applies to all repositories on your system, while the local configuration applies only to the specific repository where it is set

**Verification: Always verify your settings using git config `--list` to ensure they are correctly applied**

**Privacy: If you prefer to keep your real name private, you can use any text as your Git username, and in GitHub repositories you can use a `noreply` email to keep your's private [(see how)](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address).**

By setting your Git username and email address, you ensure that your commits are properly attributed, making collaboration and tracking changes more efficient.
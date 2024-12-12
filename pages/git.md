# Git
Git is a version control system that helps you manage different versions of code within a repository.

## Setup

### Windows

1. Download Git:
    Go to the Git for Windows [website](https://git-scm.com/downloads/win).
    Click on the "Download" button to get the latest version of Git for Windows.
    
2. Run the Installer:
    Once the download is complete, locate the downloaded file (`Git-<version>-64-bit.exe`) in your Downloads folder.
    Double-click the installer to run it.

3. Verify the Installation:
    Open the Command Prompt or Git Bash.
    Type `git --version` and press Enter. You should see the installed version of Git displayed.

### Linux

1. Install Git: 
    After updating the package index, install Git by running:
    ``` sh
    sudo apt install git
    ```

2. Verify the installation: 
    Once the installation is complete, you can verify that Git was installed correctly by checking the version:
    ``` sh
    git --version
    ```
    This should output the installed version of Git, confirming that it is installed.

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
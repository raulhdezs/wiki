# Overview

GitHub Cli, or `gh`, is a command-line interface to GitHub for use in your terminal or your scritps.

# Installing on Linux

```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```

# Configuration
- Run `gh auth login`to authenticate with your GitHub account.

# Examples of use
## Cloning a repository
### Using OWNER/REPO syntax
You can clone any repository using OWNER/REPO syntax.
```
# Cloning a repository
~/git$ gh repo clone owner/repo
Cloning into 'repo'...
~$
```

### Using other selectors
You can also use GitHub URLs to clone repositories.
```bash
# Cloning a repository
~/git$ gh repo clone https://github.com/owner/repo
Cloning into 'repo'...
~$
```
## Creating repositories
### With no arguments
Inside a git repository, and with no arguments, `gh` will automatically create a repository on GitHub on your account for your current directory, using the directory name.
```bash
~/git/my-project$ gh repo create
Created repository under user/my-project on GitHub
Added remote https://github.com/user/my-project.git
~$
```

### Setting a repository name
Enter a name to set a repository name other than the directory name.
```bash
~/git/my-project$ gh repo create my-cool-project
Created repository under user/my-cool-project on GitHub
Added remote https://github.com/user/my-cool-project.git
~$
```

## Viewing a repository
### In terminal
By default, we will display items in the terminal
```bash
~$ gh repo view owner/repo
owner/repo
Repository description

  Repository README
  
View this repository on GitHub: https://github.com/owner/repo
~$
```
### In the browser

Quickly open an item in the browser using `--web` or `-w`
```bash
~$ gh repo view owner/repo --web
Opening hhtps://github.com/owner/repo/ in your browser.r/repo
~$
```

### With no arguments
We will display the repository you're currently in.

By default, we will display items in the terminal
```bash
~/git/my-project$ gh repo view
user/my-project
Repository description

  Repository README
  
View this repository on GitHub: https://github.com/user/my-project
~$
```
## Removing a repository
Delete a GitHub repository
```bash
gh repo delete [<repository>] [flags]
```
Deletion requires authorization with the "delete_repo" scope. To authorize, run `gh auth refresh -s delete_repo`.

## List repositories
List repositories owned by user or organization
```bash
gh repo list [<owner>] [flags]
```

## Rename a repository
Rename a GitHub repository
```bash
gh repo rename [<new-name>] [flags]
```
By default, this renames the current repository.


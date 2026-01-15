# GitHub Basics

## What is GitHub?

GitHub is an online platform used to store Git repositories.  
It helps developers share code and work together on projects.

Popular alternatives:
- GitLab
- Bitbucket
- Azure Repos
- Gitea  

GitHub is the most widely used.


## Create a GitHub Account

1. Go to https://github.com
2. Click **Sign up**
3. Enter email, username, and password
4. Complete verification


## Configure Git 

Set your name and email (used in commits):

```bash
git config --global user.name "Your Name"

git config --global user.email "your-email@example.com"
```

Check configuration:

```bash
git config --list
```

## Push Code to GitHub

Initialize and commit your project:

```bash
git init

git add .

git commit -m "initial commit"
```

Add remote repository:
```bash
git remote add origin <remote-url>
```

Push code:
```bash
git push -u origin main
```

## Work with Remote Repositories
### Fetch Code

Downloads updates without merging:

```bash
git fetch origin
```

### Pull Code

Downloads and merges updates:
```bash
git pull origin main
```


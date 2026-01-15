## Git

- Git is a tool used to track changes in files, mainly source code. It helps developers save versions of their work and go back if something breaks.

- Multiple people can work on the same project without conflicts.

- Git also keeps a complete history of who changed what and when.

## Git Installation Guide

This document explains how to install and set up Git.

---

### 1. Check if Git Is Already Installed

Open your terminal or command prompt and run:

```bash
git --version
```

### 2. Download Git

1. Open a browser and go to : https://git-scm.com/install/windows
2. Click **Download for Windows**
3. The Git installer (`.exe`) will download automatically

### 3. Install and Verify Git

- Keep the default installation settings

- Complete the installation

Verify :
```bash
git --version
```
### 4. Configure Git (First-Time Setup)

Set username:

```bash
git config --global user.name "Your Name"
```

Set email:
```bash
git config --global user.email "your@email.com"
```
Verify configuration:
```bash
git config --list
```

### 5. Set Default Branch Name as Main (Optional)
```bash
git config --global init.defaultBranch main
```
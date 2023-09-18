---
title: Introduction to Git
author: Pedro Soares
header: LOSC - Luxembourg Open-Source Club
footer: Pedro Soares
theme: dracula
paginate: true
marp: true
---

# Introduction to Git & GitHub

A short introduction to the basics usage of git & GitHub

![bg right](./imgs/git-mascot.jpg)

<style scoped>
h1 {
    padding-top: 1.5em;
}
</style>

---

# What is Git?

Git is a Distributed Version Control System (DVCS) which can be used to keep track of different file versions (Snapshots).

![bg blur](./imgs/git-log.jpg)

---

# Git States

Git has 3 different states:

- **Modified:** Any file that has been changed but not yet commited
- **Staged:** Marked modified files that are ready to be commited to the next snapshot
- **Committed:** Permanently stores the staged files as a snapshot into Git directory

<!-- ![bg blur](./imgs/git-log.jpg) -->

---

# Git Workflow

A simple git workflow looks like:

1. Modify files in the worktree
1. Selectively select the modified files to be staged
1. Commit the staged files

<!-- ![bg blur](./imgs/git-log.jpg) -->

---

# Git VS GitHub

- Git is a program that runs on computer locally.

- GitHub is a platform that hosts a git directory on the cloud.

---

# Creating a Basic Config

```sh
git config --global user.name "Pedro Soares"
git config --global user.email "pedro@gmail.com"
git config --global core.editor nvim
```

---

# Staging/Adding Files

```sh
git add file_name # Stages just the specifed file
git add . # Adds all modified files from within the current directory
```

---

# Commiting Staged Files

```sh
git commit # Will open the editor of choice
git commit -m "A commit message"
git commit -a -m "Stages all files and commits with a message"
```

---

# Push & Pull from remote repo

```sh
git pull
git push
```

---

# Comparison of Changes

```sh
git diff
```

---

# Log of all the commits

```sh
git log
git log --graph
```

---

# Setting up SSH keys

```sh
ssh-keygen -t ed25519 -C "your email used with github"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

---

# A workflow Example

Demonstration ...

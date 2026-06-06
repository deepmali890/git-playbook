# Understanding .git Folder

## Introduction

The .git folder is the hidden directory that stores all Git repository information.

Whenever you run:

```bash
git init
```

Git creates a hidden .git folder inside your project.

This folder contains everything Git needs to manage:

* Commit history
* Branches
* Tags
* Configuration
* Staged changes
* Repository metadata

Without the .git folder, Git cannot track your project.

---

# What is the .git Folder?

The .git folder acts as Git's database.

Think of it as the brain of your repository.

Example:

```text
my-project/
│
├── src/
├── README.md
└── .git/
```

All Git-related information is stored inside:

```text
.git/
```

---

# Important Components

## 1. objects

Location:

```text
.git/objects
```

Purpose:

Stores all Git data.

This includes:

* Files
* Commits
* Directories

Git saves everything as objects.

---

### Types of Objects

#### Blob

Stores file content.

Example:

```text
hello.txt
```

Content is stored as a blob object.

---

#### Tree

Represents folders.

Example:

```text
src/
 ├── app.js
 └── index.js
```

Git stores folder structure as tree objects.

---

#### Commit

Stores:

* Author
* Date
* Message
* Snapshot

Example:

```bash
git commit -m "Add login page"
```

Creates a commit object.

---

# 2. refs

Location:

```text
.git/refs
```

Purpose:

Stores references to branches and tags.

Example:

```text
refs/
├── heads/
├── tags/
└── remotes/
```

---

### refs/heads

Stores local branches.

Example:

```text
main
feature-login
develop
```

---

### refs/tags

Stores tags.

Example:

```text
v1.0
v2.0
```

---

### refs/remotes

Stores remote branch references.

Example:

```text
origin/main
origin/develop
```

---

# 3. HEAD

Location:

```text
.git/HEAD
```

Purpose:

Points to the current branch or commit.

Example:

```text
ref: refs/heads/main
```

Meaning:

```text
Current branch = main
```

If you switch branches:

```bash
git switch feature-login
```

HEAD becomes:

```text
ref: refs/heads/feature-login
```

---

# 4. config

Location:

```text
.git/config
```

Purpose:

Stores repository configuration.

Example:

```ini
[remote "origin"]
url = https://github.com/user/repo.git
```

Contains:

* Remote URLs
* Branch settings
* Repository configuration

---

# 5. Index (Staging Area)

Location:

```text
.git/index
```

Purpose:

Stores staged changes before commit.

Example:

```bash
git add app.js
```

The file is added to:

```text
.git/index
```

before commit.

---

# Workflow Example

```text
Working Directory
        ↓
git add
        ↓
Index (Staging Area)
        ↓
git commit
        ↓
Objects Database
```

---

# Why is .git Important?

Benefits:

* Stores project history
* Enables branching
* Enables merging
* Enables recovery
* Tracks commits
* Stores tags
* Stores remote information

Without .git:

```bash
git status
```

will not work.

---

# Real-World Example

Suppose you have:

```text
E-Commerce Project
```

You run:

```bash
git init
```

Git creates:

```text
.git/
```

Then:

```bash
git add .
git commit -m "Initial commit"
```

Git stores:

* Files → objects
* Commit → commit object
* Branch → refs
* Current branch → HEAD

Everything is managed inside the .git folder.

---

# Common Commands

Show hidden files:

Linux / Mac:

```bash
ls -la
```

Windows PowerShell:

```powershell
dir -force
```

View Git directory:

```bash
cd .git
```

Check current branch reference:

```bash
cat HEAD
```

---

# Quick Revision

objects
→ Stores data

refs
→ Stores branches and tags

HEAD
→ Current branch pointer

config
→ Repository settings

index
→ Staging area

---

# Quiz

### Which component stores staged changes?

Answer:

```text
.git/index
```

### Which file stores current branch information?

Answer:

```text
.git/HEAD
```

### Which folder stores Git objects?

Answer:

```text
.git/objects
```
    
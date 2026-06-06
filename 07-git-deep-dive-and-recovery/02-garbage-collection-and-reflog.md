# Garbage Collection & Reflog in Git

## Introduction

Git provides powerful recovery and maintenance tools that help developers manage repositories efficiently. Two important concepts are:

* Garbage Collection (GC)
* Reflog

Garbage Collection optimizes repository storage and performance, while Reflog helps recover lost commits, deleted branches, and accidental changes.

---

# Garbage Collection (GC)

## What is Garbage Collection?

Garbage Collection is Git's cleanup mechanism that:

* Removes unnecessary objects.
* Compresses repository data.
* Optimizes storage.
* Improves Git performance.

Think of it as cleaning unused files from a storage room.

---

## Run Garbage Collection

```bash
git gc
```

When executed, Git:

* Packs loose objects into pack files.
* Removes unreachable objects.
* Compresses repository data.
* Improves repository efficiency.

---

## When Should You Use Git GC?

Use it after:

* Large merges
* Multiple rebases
* Deleting many branches
* Large numbers of commits

---

# Reflog

## What is Reflog?

Reflog (Reference Log) records every movement of:

* HEAD
* Branches
* Checkouts
* Merges
* Rebases
* Resets

Even if a commit disappears from `git log`, it can often still be recovered using Reflog.

---

## View Reflog

```bash
git reflog
```

Example:

```bash
a1b2c3d HEAD@{0}: commit: Add login feature

e4f5g6h HEAD@{1}: reset: moving to HEAD~1

i7j8k9l HEAD@{2}: checkout: moving from main to feature-login
```

---

# Recovering Lost Commits

## Scenario

Suppose you accidentally run:

```bash
git reset --hard HEAD~1
```

Your latest commit disappears.

---

## Recovery Steps

### Step 1: View Reflog

```bash
git reflog
```

Example:

```bash
abc1234 HEAD@{1}: commit: Add payment feature
```

### Step 2: Restore Commit

```bash
git reset --hard abc1234
```

Your lost commit is restored.

---

# Recovering Deleted Branches

## Scenario

You accidentally delete a branch:

```bash
git branch -D feature-login
```

---

## Recovery

Find the last commit using:

```bash
git reflog
```

Create the branch again:

```bash
git checkout -b feature-login abc1234
```

Branch successfully restored.

---

# Cherry-Pick Lost Commit

If you only need one specific commit:

```bash
git cherry-pick abc1234
```

This copies that commit into your current branch.

---

# Reflog Expiration

Git automatically removes old Reflog entries.

## Default Settings

### Reachable Commits

```text
90 Days
```

### Unreachable Commits

```text
30 Days
```

---

## Configure Reflog Expiration

```bash
git config gc.reflogExpire 90.days
```

```bash
git config gc.reflogExpireUnreachable 30.days
```

---

# Important Commands

## Run Garbage Collection

```bash
git gc
```

## View Reflog

```bash
git reflog
```

## Restore Repository State

```bash
git reset --hard <commit-hash>
```

## Recover Deleted Branch

```bash
git checkout -b <branch-name> <commit-hash>
```

## Restore Specific Commit

```bash
git cherry-pick <commit-hash>
```

---

# Real-World Example

Suppose you are maintaining your Git Learning Repository.

You create the following commits:

```bash
git commit -m "Add Gitflow notes"
```

```bash
git commit -m "Add Git Hooks notes"
```

```bash
git commit -m "Add Reflog notes"
```

Later, you accidentally run:

```bash
git reset --hard HEAD~3
```

All three commits disappear.

Check Reflog:

```bash
git reflog
```

Output:

```bash
abc1234 HEAD@{1}: commit: Add Reflog notes

def5678 HEAD@{2}: commit: Add Git Hooks notes

ghi9012 HEAD@{3}: commit: Add Gitflow notes
```

Recover:

```bash
git reset --hard abc1234
```

All commits return successfully.

---

# Quick Revision

| Command            | Purpose                       |
| ------------------ | ----------------------------- |
| `git gc`           | Clean and optimize repository |
| `git reflog`       | View HEAD history             |
| `git reset --hard` | Restore previous state        |
| `git cherry-pick`  | Reuse a specific commit       |
| `git checkout -b`  | Recover deleted branch        |

---

# Key Takeaways

* Git GC cleans and optimizes repositories.
* Reflog tracks every HEAD movement.
* Lost commits can often be recovered using Reflog.
* Deleted branches can be restored if commit hashes are available.
* Reflog acts as Git's recovery system and safety net.

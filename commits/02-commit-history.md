# Viewing Commit History

## Why View Commit History?

Git stores every commit made in a project.

Commit history helps:

* Track changes
* Find bugs
* Review code
* Understand project evolution

---

## View All Commits

### Command

```bash
git log
```

### Example Output

```text
commit a1b2c3d
Author: Dileep Mali
Date: 2026-06-06

Add login functionality
```

### Meaning

Shows:

* Commit Hash
* Author
* Date
* Commit Message

---

## Short Commit History

### Command

```bash
git log --oneline
```

### Example Output

```text
a1b2c3 Add login functionality
d4e5f6 Fix navbar bug
g7h8i9 Update README
```

### Meaning

Displays commit history in a compact format.

---

## Visual Commit Graph

### Command

```bash
git log --graph --decorate --oneline
```

### Purpose

Shows:

* Branches
* Merges
* Commit relationships

Useful for understanding branching history.

---

## View a Specific Commit

### Command

```bash
git show <commit-hash>
```

### Example

```bash
git show a1b2c3
```

### Meaning

Shows:

* Commit details
* Files changed
* Added lines
* Removed lines

---

## Compare Changes

### Command

```bash
git diff
```

### Meaning

Shows changes that are not committed yet.

---

## Compare Two Commits

### Command

```bash
git diff <commit1> <commit2>
```

### Example

```bash
git diff a1b2c3 d4e5f6
```

Shows differences between two commits.

---

## Compare Two Branches

### Command

```bash
git diff main feature-login
```

Shows differences between branches.

---

## Compare Current Commit with Previous

### Command

```bash
git diff HEAD~1 HEAD
```

### Meaning

Compare current commit with previous commit.

---

## Common Commands

### Full History

```bash
git log
```

### Short History

```bash
git log --oneline
```

### Specific Commit

```bash
git show <commit-hash>
```

### Compare Changes

```bash
git diff
```

---

## Real-World Example

Bug appears after a recent update.

Steps:

```bash
git log --oneline
```

Find suspicious commit.

```bash
git show <commit-hash>
```

Inspect changes.

```bash
git diff
```

Compare versions and identify the issue.

---

## Quick Notes

* git log = View commit history
* git show = Inspect one commit
* git diff = Compare changes
* Commit Hash uniquely identifies a commit
* Useful for debugging and code reviews

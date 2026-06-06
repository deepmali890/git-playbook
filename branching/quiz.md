# Merging Branches

## What is Merging?

Merging combines changes from one branch into another branch.

### Simple Meaning

```text
Merge = Combine Changes
```

---

## Basic Merge Workflow

### Step 1: Switch to Target Branch

```bash
git switch main
```

### Step 2: Merge Source Branch

```bash
git merge feature-login
```

### Meaning

Merge changes from `feature-login` into `main`.

---

## Fast-Forward Merge

Occurs when the target branch has no new commits.

### Example

```text
main
 │
 ▼
A

feature-login
 │
 ▼
A → B → C
```

Command:

```bash
git switch main
git merge feature-login
```

Result:

```text
main
 │
 ▼
A → B → C
```

No extra merge commit is created.

---

## Three-Way Merge

Occurs when both branches have their own commits.

### Example

```text
main
 │
 ▼
A → D

feature-login
 │
 ▼
A → B → C
```

Command:

```bash
git switch main
git merge feature-login
```

Result:

```text
A → B → C
 \       /
  \     /
   D → M
```

`M` = Merge Commit

Git creates a new commit to combine both histories.

---

## Merge Conflicts

A conflict occurs when two branches modify the same code.

### Example

```text
main:
Hello Dileep

feature-login:
Hello User
```

Git cannot decide which version to keep.

---

## Resolve Conflicts

### Check Conflict

```bash
git status
```

### Edit File

Remove conflict markers and keep the desired code.

### Stage Changes

```bash
git add .
```

### Complete Merge

```bash
git commit -m "Resolved merge conflict"
```

---

## Common Commands

### Merge Branch

```bash
git merge feature-login
```

### Check Status

```bash
git status
```

### Complete Conflict Resolution

```bash
git add .
git commit -m "Resolved merge conflict"
```

---

## Real-World Example

```text
main
 ├── Payment Feature
 ├── Dashboard Feature
 └── Login Feature
```

Each feature is developed in a separate branch and merged into `main` after testing.

---

## Quick Notes

* Merge = Combine branches
* Fast-Forward = No merge commit
* Three-Way = Creates merge commit
* Conflicts must be resolved manually
* Always merge into the target branch

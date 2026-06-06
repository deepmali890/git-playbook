# Understanding HEAD & Branches

## What is HEAD?

HEAD is a pointer that indicates the current branch and latest commit you are working on.

### Simple Meaning

```text
HEAD = Current Position in Git
```

Whenever you create a new commit, HEAD moves to that latest commit.

---

## What is a Branch?

A branch is an independent line of development.

It allows you to work on features, bug fixes, or experiments without affecting the main codebase.

### Simple Meaning

```text
Branch = Separate Workspace
```

---

## Relationship Between HEAD and Branches

### Key Points

* HEAD always points to the current branch.
* When you switch branches, HEAD moves to that branch.
* Branches are pointers to commits.

### Example

```text
main
 │
 ▼
Commit A ← HEAD
```

After switching:

```text
feature-login
      │
      ▼
   Commit A ← HEAD
```

---

## Create a Branch

```bash
git branch feature-login
```

Creates a new branch.

### Command Breakdown

* `git` → Git tool
* `branch` → Create/manage branches
* `feature-login` → Branch name

---

## Create and Switch Together

```bash
git switch -c feature-login
```

### Command Breakdown

* `switch` → Change branch
* `-c` → Create new branch
* `feature-login` → Branch name

---

## Switch Branch

```bash
git checkout feature-login
```

or

```bash
git switch feature-login
```

Moves HEAD to the selected branch.

---

## Merge Branches

```bash
git checkout main
git merge feature-login
```

### Meaning

Merge changes from `feature-login` into `main`.

---

## Benefits of Branching

* Parallel Development
* Feature Isolation
* Easier Collaboration
* Safe Experimentation
* Better Code Management

---

## Real-World Example

```text
main
 │
 ├── feature-login
 ├── feature-payment
 └── feature-dashboard
```

Each developer works on a separate branch and merges changes into `main` after testing.

---

## Quick Notes

* HEAD = Current Position
* Branch = Separate Development Line
* HEAD moves when switching branches
* Use branches for features and bug fixes
* Merge branches after testing

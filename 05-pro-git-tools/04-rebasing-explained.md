# Git Rebase

## What is Rebase?

Git rebase moves commits from one branch and reapplies them on top of another branch.

It creates a cleaner and linear commit history.

---

## Rebase vs Merge

### Merge

```bash
git merge feature-login
```

Creates a merge commit.

History remains unchanged.

---

### Rebase

```bash
git rebase main
```

Moves feature branch commits on top of main.

Creates a cleaner history.

---

## Basic Rebase

### Step 1

```bash
git checkout feature-login
```

Switch to feature branch.

### Step 2

```bash
git rebase main
```

Reapply feature branch commits on top of main.

---

## Rebase Workflow

```bash
git checkout feature-login

git rebase main
```

Result:

* Latest main changes included
* Linear history created

---

## Resolve Conflicts

If conflict occurs:

### Check Files

```bash
git status
```

### Resolve Conflict

Edit files manually.

### Stage Files

```bash
git add .
```

### Continue Rebase

```bash
git rebase --continue
```

---

## Abort Rebase

```bash
git rebase --abort
```

Cancels rebase operation.

Returns branch to previous state.

---

## Interactive Rebase

### Command

```bash
git rebase -i HEAD~3
```

### Purpose

Allows you to:

* Reorder commits
* Edit commits
* Remove commits
* Squash commits

---

## Squash Commits

Combine multiple commits into one.

Example:

```text
Fix button color
Fix button padding
Fix button icon
```

After squash:

```text
Improve button design
```

---

## Push Rebased Branch

```bash
git push --force-with-lease origin feature-login
```

### Meaning

Safely updates remote branch after rebase.

---

## Best Practices

* Rebase local branches only
* Avoid rebasing shared branches
* Use interactive rebase before pull requests
* Use force-with-lease instead of force
* Test code after rebasing

---

## Real-World Example

Feature branch:

```text
Add Login UI
Add Validation
Add Forgot Password
```

Main branch:

```text
Fix Navbar Bug
Update Footer
```

Run:

```bash
git checkout feature-login
git rebase main
```

Feature branch now includes latest main changes with clean history.

---

## Quick Revision

```text
git rebase main
→ Reapply commits on top of main

git rebase --continue
→ Continue after conflict

git rebase --abort
→ Cancel rebase

git rebase -i HEAD~3
→ Interactive rebase

git push --force-with-lease
→ Push rebased branch
```

# Creating & Switching Branches

## Why Use Branches?

Branches allow developers to work on features, bug fixes, or experiments without affecting the main codebase.

### Benefits

* Parallel Development
* Feature Isolation
* Better Collaboration
* Safe Testing

---

## Create a Branch

### Syntax

```bash
git branch <branch-name>
```

### Example

```bash
git branch feature-login
```

### Meaning

Creates a new branch but does not switch to it.

---

## Switch Branch

### Using Checkout

```bash
git checkout feature-login
```

### Using Switch (Recommended)

```bash
git switch feature-login
```

### Meaning

Moves HEAD to the selected branch.

---

## Create and Switch in One Command

### Modern Way

```bash
git switch -c feature-login
```

### Legacy Way

```bash
git checkout -b feature-login
```

### Meaning

Creates a new branch and immediately switches to it.

---

## Command Comparison

| Command                       | Action             |
| ----------------------------- | ------------------ |
| git branch feature-login      | Create branch only |
| git switch feature-login      | Switch branch      |
| git checkout feature-login    | Switch branch      |
| git switch -c feature-login   | Create + Switch    |
| git checkout -b feature-login | Create + Switch    |

---

## Branch Naming Best Practices

### Good Examples

```text
feature-login
feature-payment
bugfix-navbar
hotfix-checkout
```

### Avoid

```text
mybranch
test123
feature login
```

---

## Real-World Workflow

```bash
git switch -c feature-login
```

Develop feature

```bash
git add .
git commit -m "Added login feature"
```

Switch back

```bash
git switch main
```

Merge later

```bash
git merge feature-login
```

---

## Quick Notes

* Branch = Separate workspace
* HEAD moves when switching branches
* git switch = Modern command
* git checkout = Older command
* Use meaningful branch names

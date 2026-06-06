# Undoing Changes

## Why Undo Changes?

Git allows you to:

* Fix mistakes
* Recover previous versions
* Undo commits
* Restore files safely

---

## Git Reset

Moves the branch pointer to a previous commit.

### Types of Reset

#### Soft Reset

```bash
git reset --soft HEAD~1
```

### Meaning

* Removes last commit
* Keeps changes staged

---

#### Mixed Reset (Default)

```bash
git reset --mixed HEAD~1
```

### Meaning

* Removes last commit
* Unstages changes
* Keeps files unchanged

---

#### Hard Reset

```bash
git reset --hard HEAD~1
```

### Meaning

* Removes last commit
* Deletes all changes

⚠️ Use carefully.

---

## Git Revert

Safely undo a commit without changing history.

### Command

```bash
git revert <commit-hash>
```

### Example

```bash
git revert a1b2c3
```

### Meaning

Creates a new commit that reverses previous changes.

---

## Git Checkout

### Switch Branch

```bash
git checkout main
```

### Meaning

Move to another branch.

---

### Restore File

```bash
git checkout <commit-hash> -- app.js
```

### Meaning

Restore a file from an older commit.

---

## Command Comparison

| Command           | Purpose                            |
| ----------------- | ---------------------------------- |
| git reset --soft  | Remove commit, keep staged changes |
| git reset --mixed | Remove commit, keep files          |
| git reset --hard  | Remove commit and changes          |
| git revert        | Safely undo commit                 |
| git checkout      | Switch branch or restore file      |

---

## When to Use?

### Local Commit Mistake

```bash
git reset --mixed HEAD~1
```

### Undo Shared Commit

```bash
git revert <commit-hash>
```

### Restore Deleted File

```bash
git checkout <commit-hash> -- file-name
```

---

## Real-World Example

Wrong commit:

```bash
git commit -m "Add payment gateway"
```

Need to undo safely:

```bash
git revert <commit-hash>
```

Git creates a new commit that removes the payment gateway changes.

---

## Quick Notes

* reset = Rewrite history
* revert = Preserve history
* checkout = Restore files or switch branches
* revert is safest for shared branches
* hard reset permanently deletes changes


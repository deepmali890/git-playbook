# Git Stash

## What is Git Stash?

Git stash temporarily saves uncommitted changes without creating a commit.

It allows you to:

* Pause current work
* Switch tasks quickly
* Keep commit history clean

---

## Why Use Git Stash?

Benefits:

* Clean commit history
* Safe task switching
* Prevents loss of work
* Improves workflow efficiency

---

## Create a Stash

### Command

```bash
git stash
```

### Meaning

Temporarily saves:

* Modified files
* Staged changes

Restores working directory to last commit.

---

## Stash with Message

### Command

```bash
git stash save "Working on login feature"
```

### Meaning

Creates a stash with a custom message.

Useful when multiple stashes exist.

---

## View All Stashes

### Command

```bash
git stash list
```

### Example

```text
stash@{0}: Added login feature
stash@{1}: Navbar redesign
```

### Meaning

Shows all saved stashes.

---

## Apply Latest Stash

### Command

```bash
git stash apply
```

### Meaning

Restores latest stash.

Stash remains stored.

---

## Apply and Remove Stash

### Command

```bash
git stash pop
```

### Meaning

* Restores latest stash
* Removes it from stash list

---

## Apply Specific Stash

### Command

```bash
git stash apply stash@{1}
```

### Meaning

Restores a selected stash.

---

## Remove Latest Stash

### Command

```bash
git stash drop
```

### Meaning

Deletes most recent stash.

---

## Remove Specific Stash

### Command

```bash
git stash drop stash@{1}
```

### Meaning

Deletes selected stash.

---

## Remove All Stashes

### Command

```bash
git stash clear
```

### Meaning

Deletes all stored stashes.

---

## Best Practices

* Use stash messages
* Clean old stashes regularly
* Review stash list before applying
* Use stash for temporary work only
* Prefer commits for completed work

---

## Real-World Example

Working on login feature:

```bash
git stash save "Login feature in progress"
```

Urgent bug arrives.

Switch branch:

```bash
git switch main
```

Fix bug and commit.

Return to previous work:

```bash
git stash pop
```

Continue development from where you stopped.

---

## Quick Revision

```text
git stash
→ Save temporary changes

git stash list
→ Show stashes

git stash apply
→ Restore stash

git stash pop
→ Restore and remove stash

git stash drop
→ Delete stash

git stash clear
→ Delete all stashes
```

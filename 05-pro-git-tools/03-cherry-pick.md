# Cherry Pick

## What is Cherry Pick?

Cherry-pick allows you to copy a specific commit from one branch to another.

Instead of merging an entire branch, only selected commits are applied.

---

## Why Use Cherry Pick?

Useful when:

* Copying a bug fix
* Moving a hotfix to production
* Applying a specific feature
* Avoiding a full branch merge

---

## Find Commit Hash

### Command

```bash
git log --oneline
```

### Example

```text
a1b2c3 Fix login bug
d4e5f6 Add dashboard feature
```

### Meaning

Displays commit history with commit hashes.

---

## Cherry Pick a Commit

### Command

```bash
git cherry-pick <commit-hash>
```

### Example

```bash
git cherry-pick a1b2c3
```

### Meaning

Copies the selected commit into the current branch.

---

## Complete Workflow

### Step 1

```bash
git log --oneline
```

Find the commit hash.

### Step 2

```bash
git checkout main
```

Switch to target branch.

### Step 3

```bash
git cherry-pick a1b2c3
```

Apply selected commit.

---

## Cherry Pick Multiple Commits

### Command

```bash
git cherry-pick a1b2c3 d4e5f6 e7f8g9
```

### Meaning

Applies multiple commits in sequence.

---

## Handle Conflicts

If conflicts occur:

### Check Files

```bash
git status
```

### Resolve Conflicts

Edit conflicting files.

### Stage Files

```bash
git add .
```

### Continue

```bash
git cherry-pick --continue
```

---

## Abort Cherry Pick

### Command

```bash
git cherry-pick --abort
```

### Meaning

Cancels the cherry-pick process.

Returns repository to previous state.

---

## Best Practices

* Cherry-pick only required commits
* Check commit dependencies
* Avoid excessive cherry-picking
* Test code after cherry-pick
* Prefer merge for large changes

---

## Real-World Example

Bug fixed in:

```text
develop branch
```

Need same fix in:

```text
main branch
```

Commands:

```bash
git checkout main
git cherry-pick a1b2c3
```

Bug fix is copied without merging the entire branch.

---

## Quick Revision

```text
git log --oneline
→ Find commit hash

git cherry-pick <hash>
→ Copy specific commit

git cherry-pick --continue
→ Continue after conflict

git cherry-pick --abort
→ Cancel cherry-pick
```

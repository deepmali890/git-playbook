## Git Pull

Fetches and merges changes from a remote repository into the current branch.

### Syntax

```bash
git pull <remote-name> <branch-name>
```

### Example

```bash
git pull origin main
```

### Command Breakdown

* `git` → Git command line tool
* `pull` → Fetch + Merge changes
* `origin` → Remote repository
* `main` → Branch name

### Simple Meaning

Download the latest changes from the remote repository and merge them into the current branch.

---

### How Git Pull Works

```text
git pull
   ↓
git fetch
   ↓
git merge
```

---

### Why Use Git Pull?

* Keep local repository up to date
* Reduce merge conflicts
* Stay synchronized with the team

---

### Common Conflict

If both developers modify the same code:

```bash
git pull origin main
```

Git may create a merge conflict.

Resolve the conflict, then:

```bash
git add .
git commit -m "Resolved merge conflict"
```

---

### Best Practice

Before starting work:

```bash
git pull origin main
```

---

### Quick Notes

* `git fetch` → Download only
* `git pull` → Download + Merge
* Pull regularly before starting work

```
```

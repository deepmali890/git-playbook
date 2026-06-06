## Git Push

Uploads local commits to a remote repository.

### Syntax

```bash
git push <remote-name> <branch-name>
```

### Example

```bash
git push origin main
```

### Command Breakdown

* `git` → Git command line tool
* `push` → Upload local commits
* `origin` → Remote repository name
* `main` → Branch name

### Simple Meaning

Upload commits from the local `main` branch to the `origin` remote repository.

### Push a New Branch

```bash
git push -u origin feature-branch
```

* `-u` → Sets upstream tracking for future pushes

After this:

```bash
git push
```

is enough.

### Quick Note

* `git push` → Upload changes
* `git pull` → Download and merge changes
# Git Remotes

## What is a Remote?

A remote is a reference to a Git repository hosted on a server such as GitHub, GitLab, or Bitbucket.

Remotes help us:

* Share code
* Collaborate with others
* Backup projects
* Sync changes across devices

---

## Common Remote Names

### origin

Default remote created when a repository is cloned.

```bash
git clone <repository-url>
```

### upstream

Usually points to the original repository from which a fork was created.

Example:

```bash
git remote add upstream <repository-url>
```

---

## View All Remotes

```bash
git remote -v
```

Shows all configured remotes and their URLs.

Example Output:

```text
origin    https://github.com/user/project.git (fetch)
origin    https://github.com/user/project.git (push)
```

---

## Add a Remote

```bash
git remote add <name> <url>
```

Example:

```bash
git remote add origin https://github.com/user/project.git
```

---

## Push Changes

Upload local commits to a remote repository.

```bash
git push <remote> <branch>
```

Example:

```bash
git push origin main
```

---

## Pull Changes

Download and merge changes from a remote repository.

```bash
git pull <remote> <branch>
```

Example:

```bash
git pull origin main
```

---

## Remove a Remote

```bash
git remote remove <name>
```

Example:

```bash
git remote remove upstream
```

---

## Typical Workflow

```bash
git pull origin main
git add .
git commit -m "message"
git push origin main
```

---

## Benefits

* Collaboration
* Cloud Backup
* Version Control
* Team Synchronization

---

## Important Commands

```bash
git remote -v
git remote add <name> <url>
git push origin main
git pull origin main
git remote remove <name>
```

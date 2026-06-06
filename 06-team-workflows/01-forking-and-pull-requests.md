# Forking and Pull Requests

## What is Forking?

Forking creates your own copy of someone else's repository on GitHub.

It allows you to make changes without affecting the original repository.

---

## Why Use Forking?

Benefits:

* Safe experimentation
* Open-source contributions
* Independent development
* No direct access required

---

## Fork Workflow

```text
Original Repository
        ↓
       Fork
        ↓
      Clone
        ↓
   Create Branch
        ↓
   Make Changes
        ↓
      Commit
        ↓
       Push
        ↓
   Pull Request
```

---

## Clone Your Fork

```bash
git clone <YOUR_FORK_URL>
```

Downloads your forked repository to your local machine.

---

## Add Upstream Repository

```bash
git remote add upstream <ORIGINAL_REPO_URL>
```

Connects your fork with the original repository.

---

## Check Remotes

```bash
git remote -v
```

Example:

```text
origin     https://github.com/your-username/project.git

upstream   https://github.com/original-owner/project.git
```

---

## Create a Branch

```bash
git switch -c feature-login
```

Creates and switches to a new branch.

---

## Make Changes

Edit files as required.

---

## Stage Changes

```bash
git add .
```

Adds all modified files.

---

## Commit Changes

```bash
git commit -m "feat: add login button"
```

Creates a commit with a descriptive message.

---

## Push Changes

```bash
git push origin feature-login
```

Uploads branch to your fork.

---

## Create Pull Request

Steps:

1. Open GitHub
2. Open your fork
3. Click Pull Requests
4. Click New Pull Request
5. Select branch
6. Add title and description
7. Submit Pull Request

---

## Respond to Feedback

If reviewers request changes:

```bash
git add .
git commit -m "fix: update review suggestions"
git push origin feature-login
```

Pull Request updates automatically.

---

## Sync Fork with Original Repository

Fetch latest changes:

```bash
git fetch upstream
```

Merge changes:

```bash
git merge upstream/main
```

---

## Best Practices

* Create a new branch for every feature
* Use meaningful commit messages
* Keep pull requests small
* Sync fork regularly
* Respond politely to reviews

---

## Real-World Example

Repository:

```text
facebook/react
```

Process:

1. Fork React repository
2. Clone your fork
3. Create branch

```bash
git switch -c fix-docs
```

4. Fix documentation
5. Commit changes

```bash
git commit -m "docs: fix installation typo"
```

6. Push changes

```bash
git push origin fix-docs
```

7. Create Pull Request

---

## Quick Revision

```text
Fork
→ Copy repository

Clone
→ Download repository

Upstream
→ Original repository

Origin
→ Your fork

Pull Request
→ Request to merge changes
```

---

## Quiz

### Which command creates a branch?

Answer:

```bash
git switch -c branch-name
```

or

```bash
git checkout -b branch-name
```

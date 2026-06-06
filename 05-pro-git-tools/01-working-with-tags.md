# Working with Tags

## What are Tags?

Tags are labels that point to specific commits in Git history.

Used for:

* Software releases
* Project milestones
* Stable versions

Examples:

```text
v1.0.0
v1.1.0
v2.0.0
```

---

## Semantic Versioning (SemVer)

Format:

```text
MAJOR.MINOR.PATCH
```

Example:

```text
v1.0.0
```

### Meaning

| Part  | Purpose          |
| ----- | ---------------- |
| MAJOR | Breaking changes |
| MINOR | New features     |
| PATCH | Bug fixes        |

Examples:

```text
v2.0.0 → Major update
v1.1.0 → New feature
v1.0.1 → Bug fix
```

---

## Create a Tag

```bash
git tag v1.0.0 -m "Initial release"
```

### Meaning

Creates a tag named `v1.0.0`.

---

## Push Tag to GitHub

```bash
git push origin v1.0.0
```

### Meaning

Uploads the tag to the remote repository.

---

## Annotated Tag

```bash
git tag -a v1.1.0 -m "Fix critical bug"
```

### Meaning

Creates a tag with extra information:

* Tag name
* Message
* Creator
* Date

---

## View Tags

```bash
git tag
```

### Meaning

Shows all available tags.

---

## View Tag Details

```bash
git show v1.0.0
```

### Meaning

Displays:

* Tag message
* Commit information
* Author details

---

## Delete Local Tag

```bash
git tag -d v1.0.0
```

### Meaning

Removes tag from local repository.

---

## Delete Remote Tag

```bash
git push origin --delete v1.0.0
```

### Meaning

Removes tag from GitHub.

---

## Best Practices

* Use Semantic Versioning
* Use meaningful tag names
* Tag important releases
* Avoid deleting release tags
* Push tags after creating them

---

## Real-World Example

Release completed:

```bash
git tag -a v1.0.0 -m "Initial production release"
git push origin v1.0.0
```

Now anyone can access that exact version later.

---

## Quick Revision

```text
git tag                 → List tags

git tag v1.0.0 -m ""    → Create tag

git push origin v1.0.0  → Push tag

git show v1.0.0         → View tag

git tag -d v1.0.0       → Delete local tag

git push origin --delete v1.0.0
                         → Delete remote tag
```

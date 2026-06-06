# Making Effective Commits

## What is a Commit?

A commit is a saved snapshot of your project at a specific point in time.

### Simple Meaning

```text
Commit = Save Point
```

---

## Why Are Good Commit Messages Important?

Good commit messages help:

* Understand project history
* Improve team collaboration
* Simplify debugging
* Track changes easily
* Help future maintenance

---

## Commit Command

```bash
git commit -m "Added login feature"
```

### Breakdown

* `git` → Git tool
* `commit` → Save current changes
* `-m` → Message flag
* `"Added login feature"` → Commit message

---

## Bad Commit Messages

❌ Avoid:

```text
update
changes
fix
new code
work done
```

Reason:

```text
No clear information about what changed.
```

---

## Good Commit Messages

✅ Use clear and meaningful messages:

```text
Add user login feature
Fix navbar alignment issue
Update README documentation
Refactor payment service
Remove unused files
```

---

## Common Commit Prefixes

### Add

```text
Add login functionality
```

Used when adding something new.

---

### Fix

```text
Fix authentication bug
```

Used when fixing issues.

---

### Update

```text
Update project documentation
```

Used when modifying existing content.

---

### Refactor

```text
Refactor user service code
```

Used when improving code structure without changing functionality.

---

### Remove

```text
Remove unused CSS files
```

Used when deleting code or files.

---

## Good Commit Structure

### Subject Line

```text
Add login functionality
```

Short summary of the change.

---

### Detailed Commit

```bash
git commit
```

Example:

```text
Add login functionality

Implemented user authentication
using JWT tokens.

Added validation and error handling.
```

---

## Best Practices

* Write meaningful messages
* Keep messages short and clear
* Explain what changed
* Commit one feature at a time
* Avoid vague messages

---

## Real-World Examples

```text
Add dark mode support

Fix payment gateway timeout issue

Update portfolio README

Refactor API service layer

Remove deprecated methods
```

---

## Quick Notes

* Commit = Project snapshot
* Use meaningful messages
* Avoid generic commit names
* One commit = One logical change
* Good commits make debugging easier

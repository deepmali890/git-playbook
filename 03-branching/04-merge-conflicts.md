# Merge Conflicts

## What is a Merge Conflict?

A merge conflict occurs when Git cannot automatically combine changes from two branches.

### Simple Meaning

```text
Git is confused and needs your decision.
```

---

## Why Do Merge Conflicts Happen?

### Common Reasons

* Two developers edit the same file
* Same line is modified in different branches
* Branches become outdated before merging

---

## Example

### Main Branch

```javascript
function greet() {
    return "Hello World";
}
```

### Feature Branch

```javascript
function greet() {
    return "Hello User";
}
```

When merging, Git cannot decide which version to keep.

---

## Conflict Markers

Git adds special markers inside the file:

```text
<<<<<<< HEAD
return "Hello World";
=======
return "Hello User";
>>>>>>> feature-login
```

### Meaning

* `<<<<<<< HEAD` → Current branch code
* `=======` → Separator
* `>>>>>>> feature-login` → Incoming branch code

---

## Resolve a Conflict

### Step 1: Check Conflict

```bash
git status
```

### Step 2: Edit the File

Choose the correct code and remove conflict markers.

Example:

```javascript
function greet() {
    return "Hello User";
}
```

### Step 3: Stage Changes

```bash
git add .
```

### Step 4: Complete Merge

```bash
git commit -m "Resolved merge conflict"
```

---

## Useful Commands

### Check Status

```bash
git status
```

### Stage Resolved File

```bash
git add <file-name>
```

### Complete Merge

```bash
git commit -m "Resolved merge conflict"
```

### Open Merge Tool

```bash
git mergetool
```

---

## How to Prevent Conflicts?

### Best Practices

* Pull changes regularly

```bash
git pull origin main
```

* Communicate with team members
* Keep branches small
* Merge frequently
* Review code before merging

---

## Real-World Example

```text
Developer A
    │
    ├── Edit login.js
    │
Developer B
    │
    └── Edit login.js
```

Both modify the same line.

Result:

```text
Merge Conflict
```

Git asks developers to choose the correct version.

---

## Quick Notes

* Conflict = Git cannot decide automatically
* Resolve manually
* Remove conflict markers
* Use git add after fixing
* Complete with git commit

```
```

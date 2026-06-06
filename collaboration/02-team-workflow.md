# Team Collaboration Workflow

## Core Concepts

### Version Control

Tracks code changes over time.

**Benefits:**

* Track changes
* Restore previous versions
* Safe experimentation

---

### Branching

Creates separate lines of development.

**Use Cases:**

* New features
* Bug fixes
* Testing

**Create Branch**

```bash
git checkout -b feature-branch
```

---

### Pull Request (PR)

Used to propose changes before merging into the main branch.

**Benefits:**

* Code review
* Team discussion
* Quality assurance

---

### Merging

Combines changes from one branch into another.

Example:

```bash
git merge feature-branch
```

---

## Typical Team Workflow

### 1. Create a Branch

```bash
git checkout -b feature/add-login
```

### 2. Make Changes

Update code and test.

### 3. Commit Changes

```bash
git commit -m "Added login feature"
```

### 4. Push Branch

```bash
git push origin feature/add-login
```

### 5. Create Pull Request

Request to merge changes into `main`.

### 6. Code Review

Team reviews the code.

### 7. Merge

Approved changes are merged into `main`.

---

## Real-World Flow

```text
main
  │
  └── feature/add-login
          │
          ├── Code Changes
          ├── Commit
          ├── Push
          └── Pull Request
                    │
                    ▼
                 Review
                    │
                    ▼
                  Merge
                    │
                    ▼
                   main
```

---

## Important Commands

```bash
git checkout -b feature-name
git commit -m "message"
git push origin feature-name
git merge feature-name
```

---

## Quick Notes

* Version Control → Track changes
* Branch → Isolated development
* Pull Request → Request review
* Merge → Combine changes
* Always work in feature branches

# Reviewing and Merging Pull Requests

## Introduction

Pull Request (PR) Review is a process where team members examine code changes before they are merged into the main codebase.

The goal is to improve code quality, security, performance, and collaboration.

---

# Why Review Pull Requests?

Benefits:

* Catch bugs early
* Improve code quality
* Enforce coding standards
* Share knowledge among team members
* Prevent production issues
* Improve team collaboration

---

# Pull Request Review Checklist

Before approving a PR, review:

### Purpose

* What problem is being solved?
* Is the feature needed?
* Does it match project requirements?

### Code Quality

* Clean code
* Proper naming conventions
* Readable structure
* No duplicate code

### Functionality

* Does the feature work?
* Are edge cases handled?
* Are tests passing?

### Performance

* Efficient logic
* No unnecessary loops
* No performance bottlenecks

### Security

* Input validation
* No exposed secrets
* Safe API usage

---

# PR Review Actions

GitHub provides three common actions:

## 1. Comment

Used when asking questions or giving suggestions.

Example:

```text
Can we rename this variable for better readability?
```

---

## 2. Request Changes

Used when code needs fixes before merging.

Example:

```text
Please handle null values before merging.
```

---

## 3. Approve

Used when code looks good and is ready to merge.

Example:

```text
Looks good to me.
Approved.
```

---

# Merging Pull Requests

After approval:

1. Open Pull Request
2. Review all checks
3. Click Merge Pull Request
4. Confirm Merge

Changes become part of the target branch.

---

# Merge Strategies

## Merge Commit

Creates a new merge commit.

```text
main
  \
   feature-login
        \
      Merge Commit
```

Command:

```bash
git merge feature-login
```

---

## Squash Merge

Combines all commits into one.

Example:

```text
feat: create login page
fix: login validation
fix: login UI
```

Becomes:

```text
feat: add login feature
```

Cleaner history.

---

## Rebase Merge

Places commits on top of target branch.

Produces a linear history.

```text
main
A-B-C

feature
D-E

Result
A-B-C-D-E
```

---

# Reviewer Best Practices

* Review carefully
* Give constructive feedback
* Be respectful
* Ask questions
* Focus on code, not developer
* Review promptly

---

# Author Best Practices

* Write clear PR descriptions
* Keep PRs small
* Follow coding standards
* Add tests
* Respond to feedback quickly

---

# Real-World Example

Feature:

```text
Add Like Button
```

Problems found during review:

* No tests added
* Hardcoded user ID
* Duplicate likes allowed

Reviewer feedback:

```text
Please add unit tests.

Avoid hardcoded user IDs.

Prevent users from liking the same post multiple times.
```

Developer fixes issues and pushes updates.

Reviewer approves.

PR gets merged.

---

# Common Workflow

```text
Create Branch
      ↓
Make Changes
      ↓
Commit
      ↓
Push
      ↓
Create PR
      ↓
Review
      ↓
Fix Feedback
      ↓
Approve
      ↓
Merge
```

---

# Quick Revision

Comment
→ Ask questions

Request Changes
→ Fix required

Approve
→ Ready to merge

Merge
→ Add code to target branch

```

---

# Quiz

### What should you do before approving a PR?

Answer:

- Check code quality
- Verify functionality
- Review security
- Review performance
- Ensure tests pass
```

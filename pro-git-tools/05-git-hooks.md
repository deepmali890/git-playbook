# Git Hooks

## What are Git Hooks?

Git Hooks are scripts that run automatically before or after specific Git events.

They help automate tasks and enforce project rules.

Think of Git Hooks as automation triggers inside Git.

---

## Why Use Git Hooks?

Benefits:

* Automate repetitive tasks
* Improve code quality
* Enforce commit standards
* Prevent mistakes before pushing code
* Save development time

---

## Common Git Hooks

### 1. Pre-commit

Runs before a commit is created.

Use Cases:

* Run linting
* Check code formatting
* Run unit tests

Example:

```bash
pre-commit
```

---

### 2. Commit-msg

Runs after writing a commit message but before commit creation.

Use Cases:

* Validate commit message format
* Enforce team conventions

Example:

```bash
commit-msg
```

---

### 3. Pre-push

Runs before pushing code.

Use Cases:

* Run test cases
* Verify build success

Example:

```bash
pre-push
```

---

### 4. Post-receive

Runs on the server after code is pushed.

Use Cases:

* Auto deployment
* CI/CD pipelines

Example:

```bash
post-receive
```

---

## Hook Location

Git Hooks are stored inside:

```text
.git/hooks/
```

Example:

```text
.git/
└── hooks/
    ├── pre-commit
    ├── commit-msg
    ├── pre-push
    └── post-receive
```

---

## Creating a Hook

### Step 1

Move to hooks folder:

```bash
cd .git/hooks
```

### Step 2

Create a hook file:

```bash
touch pre-commit
```

### Step 3

Make it executable:

```bash
chmod +x pre-commit
```

### Step 4

Add script code inside it.

---

## Simple Pre-commit Hook

```bash
#!/bin/sh

echo "Running pre-commit hook..."
```

Whenever commit runs:

```bash
git commit -m "Add login page"
```

Output:

```text
Running pre-commit hook...
```

---

## Example: Commit Message Validation

```bash
#!/bin/sh

MSG_FILE=$1

if ! grep -q "^fix:" "$MSG_FILE"; then
  echo "Commit message must start with fix:"
  exit 1
fi

exit 0
```

Valid:

```bash
git commit -m "fix: login validation bug"
```

Invalid:

```bash
git commit -m "login validation bug"
```

Commit will be blocked.

---

## Example: Pre-Push Hook

```bash
#!/bin/sh

echo "Running tests..."

./run_tests.sh
```

If tests fail:

```text
Push aborted
```

If tests pass:

```text
Push successful
```

---

## Best Practices

* Keep hooks lightweight
* Use hooks for automation
* Validate commit messages
* Run tests before push
* Share hooks with team using setup scripts

---

## Real-World Use Cases

### Code Quality

Before commit:

```text
Run ESLint
Run Prettier
Run Unit Tests
```

If anything fails:

```text
Commit Blocked
```

---

### Deployment Automation

After pushing to main:

```text
Pull latest code
Build project
Deploy application
Restart server
```

All automatically.

---

## Quick Revision

```text
pre-commit
→ Runs before commit

commit-msg
→ Validates commit message

pre-push
→ Runs before push

post-receive
→ Runs after push on server

.git/hooks/
→ Hook location
```

---

## Quiz Answers

### Which hook runs before commit?

Answer:

```text
pre-commit
```

### Which hook validates commit messages?

Answer:

```text
commit-msg
```

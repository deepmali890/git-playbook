# Module 2 Quiz

## Q1. What does `origin` refer to?

* Local PC
* ✅ Default remote repository
* Branch
* Folder

**Answer:** Default remote repository

**Explanation:**
`origin` is the default name given to the remote repository when a project is cloned.

---

## Q2. What does `git pull` do?

* Upload changes
* ✅ Fetch + Merge changes
* Delete files
* Hide changes

**Answer:** Fetch + Merge changes

**Explanation:**
`git pull` downloads the latest changes from a remote repository and merges them into the current local branch.

Example:

```bash
git pull origin main
```

---

## Q3. What does `git fetch` do?

* Merge changes automatically
* Commit changes
* Delete files
* ✅ Download changes only

**Answer:** Download changes only

**Explanation:**
`git fetch` downloads the latest changes from the remote repository but does not merge them into the current branch.

Example:

```bash
git fetch origin
```

---

## Q4. What is `git push` used for?

* ✅ Upload commits
* Download changes
* Delete files
* Merge branches

**Answer:** Upload commits

**Explanation:**
`git push` uploads local commits from your repository to a remote repository such as GitHub.

Example:

```bash
git push origin main
```

---

## Q5. What does `git remote` do?

* Delete repository
* Print output
* ✅ Manage and link remote repositories
* Shutdown Git

**Answer:** Manage and link remote repositories

**Explanation:**
`git remote` is used to view, add, remove, and manage connections between a local repository and remote repositories.

Example:

```bash
git remote -v
```

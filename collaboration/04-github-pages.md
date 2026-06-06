# GitHub Pages Demo

## Goal

Deploy a static website using GitHub Pages.

---

## Website Files

```text
project/
├── index.html
├── style.css
├── script.js
└── assets/
```

### Main File

```text
index.html
```

---

## Create Repository

Example:

```text
dileep-portfolio
```

or

```text
username.github.io
```

---

## Upload Website Files

### Using Git

```bash
git clone <repository-url>
git add .
git commit -m "Initial website"
git push origin main
```

### Command Breakdown

* `git clone` → Download repository locally
* `git add .` → Stage all files
* `git commit` → Save changes
* `git push` → Upload files to GitHub

---

## Enable GitHub Pages

```text
Repository
   ↓
Settings
   ↓
Pages
   ↓
Source: main
   ↓
Save
```

---

## Website URL

### User Site

Repository:

```text
username.github.io
```

URL:

```text
https://username.github.io
```

### Project Site

Repository:

```text
my-portfolio
```

URL:

```text
https://username.github.io/my-portfolio
```

---

## Custom Domain

Example:

```text
www.dileepmali.com
```

Can be connected through DNS settings.

---

## Common Uses

* Portfolio Website
* Resume Website
* Project Showcase
* Documentation
* Personal Blog

---

## Advanced Features

* Custom Domain
* Jekyll Themes
* Custom 404 Page
* GitHub Actions (CI/CD)

---

## Quick Notes

* GitHub Pages = Free Static Hosting
* Main File = index.html
* Supports HTML, CSS, JS
* Hosted directly from GitHub Repository
* Great for Portfolio Projects

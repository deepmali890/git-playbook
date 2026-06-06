## Git Push

### What is Git Push?

Local commits ko remote repository (GitHub) par upload karta hai.

```bash
git push origin main
```

### Meaning

* git push → upload changes
* origin → remote repository
* main → branch name

### When to Use?

Jab local commits ko GitHub par bhejna ho.

### New Branch Push

```bash
git push -u origin feature-branch
```

`-u` future pushes ke liye tracking set karta hai.

Baad me sirf:

```bash
git push
```

### Common Issue

Push reject ho jaye:

```bash
git pull origin main
```

Latest changes lo aur phir push karo.

### Quick Note

```text
git push = Upload Changes
git pull = Download Changes
```

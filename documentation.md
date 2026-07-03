# CI-Test Project

This project is created to learn Git, GitHub, and GitHub Actions (CI/CD).

---

## Project Files

- main.py
- my_tools.py
- .gitignore
- .github/workflows/python-ci.yml

---

## Workflow

### Step 1
Open the project in VS Code.

### Step 2
Write or modify the Python code.

Example:

```python
from my_tools import greet

print(greet("Mithun"))
```

### Step 3
Save all files.

Shortcut:

```
Ctrl + S
```

or

```
Cmd + S (Mac)
```

---

### Step 4
Check Git status

```bash
git status
```

---

### Step 5
Stage the changes

```bash
git add .
```

or

```bash
git add main.py
```

---

### Step 6
Create a commit

```bash
git commit -m "Added greeting function"
```

Always write meaningful commit messages.

Examples

```
Initial CI test
Added greeting function
Updated main.py
Renamed utils.py to my_tools.py
Added .gitignore
Fixed import error
```

---

### Step 7
Push to GitHub

```bash
git push origin main
```

---

### Step 8
GitHub Actions starts automatically.

Go to

Actions

and verify that the workflow shows

✅ Passed

instead of

❌ Failed

---

## Learning Notes

Things learned

- Git status
- Git add
- Git commit
- Git push
- GitHub Actions
- CI/CD Pipeline
- Python modules
- Importing functions
- .gitignore
- Workflow debugging

---

## Author

Mithun N Naik
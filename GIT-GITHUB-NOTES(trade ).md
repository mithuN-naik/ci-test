Git & GitHub Workflow (Trading Automation Project)
Goal
Create a Python project on your Mac, track it with Git, and back it up to a private GitHub repository.
Step 1: Create a Project Folder
Create a folder:
trading-automation-python
Example:
trading-automation-python/
Step 2: Activate Conda Environment
conda activate quantra_py
Verify:
conda info --envs
You should see:
* quantra_py
Step 3: Go to Your Project
cd ~/trading-automation-python
Verify:
pwd
Output:
/Users/mithun123/trading-automation-python
Step 4: Check Files
ls
Example:
INFY.csv
infy.ipynb
infy2.ipynb
Step 5: Initialize Git
git init
Git creates:
.git/
This hidden folder stores:
Commit history
Branches
Configuration
Project versions
Step 6: Create .gitignore
touch .gitignore
Open:
nano .gitignore
Add:
# Jupyter
.ipynb_checkpoints/

# Python
__pycache__/
*.pyc

# macOS
.DS_Store

# Conda
.env
.venv

# Log files
*.log
Save:
Ctrl + O
Enter
Ctrl + X
Step 7: Check Hidden Files
ls -a
Example:
.git
.gitignore
.ipynb_checkpoints
INFY.csv
infy.ipynb
infy2.ipynb
Step 8: Check Git Status
git status
Git tells you:
Modified files
New files
Deleted files
Step 9: Stage Files
git add .
Meaning:
"Prepare everything for the next commit."
Step 10: Check Status Again
git status
You should see:
Changes to be committed:
Step 11: Commit
git commit -m "Initial commit - Quant trading practice"
Meaning:
Take a permanent snapshot of the project.
Step 12: Create GitHub Repository
On GitHub:
New Repository
Repository name:
trading-automation-python
Choose:
✅ Private
Do NOT add:
README
.gitignore
License
Step 13: Connect Local Project to GitHub
git remote add origin git@github.com:mithuN-naik/trading-automation-python.git
Meaning:
Connect this local project to GitHub.
Step 14: Rename Default Branch
git branch -M main
Step 15: Upload Project
git push -u origin main
Meaning:
Upload every committed file to GitHub.
Result
Mac
trading-automation-python
│
├── .git
├── .gitignore
├── infy.ipynb
├── infy2.ipynb
└── INFY.csv
↓
GitHub
trading-automation-python
│
├── .gitignore
├── infy.ipynb
├── infy2.ipynb
└── INFY.csv
GitHub becomes an online backup.
Daily Workflow
Open Terminal
conda activate quantra_py
cd ~/trading-automation-python
Open Jupyter
jupyter notebook
Write code.
Save notebook.
At the End of the Day
Check changes
git status
Stage files
git add .
Commit
git commit -m "Added RSI strategy"
Upload
git push
Done.
Useful Git Commands
Current folder
pwd
List files
ls
List hidden files
ls -a
Status
git status
Add all files
git add .
Commit
git commit -m "message"
Upload
git push
Download latest changes
git pull
View commit history
git log --oneline
See remote repository
git remote -v
What .gitignore Does
It tells Git:
Ignore these files.
Ignored:
.ipynb_checkpoints/
Jupyter backup notebooks.
Ignored:
__pycache__/
Python cache.
Ignored:
*.pyc
Compiled Python files.
Ignored:
.DS_Store
macOS system file.
Ignored:
*.log
Log files.
Ignored:
.env
Secrets/API keys.
Ignored:
.venv
Virtual environment.
Git Workflow Diagram
Write Code
     │
     ▼
Save Notebook
     │
     ▼
git status
     │
     ▼
git add .
     │
     ▼
git commit
     │
     ▼
git push
     │
     ▼
GitHub Backup
Important Concept
Your project exists in two places.
Local copy:
Mac
Remote copy:
GitHub
git push copies your committed changes from your Mac to GitHub.
git pull copies changes from GitHub back to your Mac.
My recommendation
Keep this as your standard workflow for every Python, cybersecurity, or trading project you create. Repeating the same sequence each time is how these commands become familiar—you'll soon find yourself typing them without needing to look them up.
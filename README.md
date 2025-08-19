# Git Cheatsheet Repository

Welcome to my Git Cheatsheet repository! This repo contains a comprehensive collection of essential Git commands, workflows, and best practices that I use daily to manage my projects efficiently.

Whether you are a beginner or an experienced developer, this cheatsheet will help you quickly reference key Git operations and improve your version control skills.

Feel free to explore, learn, and contribute!

---

*Below is the detailed Git cheatsheet for quick reference and daily use.*


# COMPLETE GIT CHEATSHEET (EXPLANATIONS + UNIVERSAL PLACEHOLDERS)

## 1. REPOSITORY SETUP
```bash
git --version                     # Verify Git installation
git status                       # Check repo status (should show "not a git repo")
git init                        # Initialize new repo (creates .git folder)
git init -b        # Initialize with specific branch (main/master)

# Remove repository:
rm -rf .git                     # Delete .git folder via terminal
# OR delete .git folder manually in file explorer
```

## 2. BASIC WORKFLOW
*Working Directory → Staging Area → Repository*
```bash
git add                   # Stage specific file (e.g., FirstCode.txt)
git status                      # Shows staged (green) vs unstaged (red) files
git commit -m "" # Commit staged files with message
git log                        # View commit history (q to exit)
```

## 3. MAKING CHANGES
```bash
git add          # Stage modified file
git commit -m ""   # Commit changes
git commit -a -m ""    # Skip staging (auto-adds tracked files)
```

## 4. INSPECTING CHANGES
```bash
git diff                       # Show unstaged changes
git diff --staged              # Show staged changes
git show          # View specific commit changes
```

## 5. MULTI-FILE OPERATIONS
```bash
git add .                      # Stage all files
git add *.txt                  # Stage all .txt files
git add /              # Stage entire folder
```

## 6. UNDOING CHANGES
```bash
git restore              # Discard unstaged changes
git restore --staged     # Unstage file
git commit --amend             # Fix last commit's message/content
```

## 7. REMOTE REPOSITORIES
```bash
git clone            # Clone repo (HTTPS/SSH)
git remote add origin  # Add remote origin
git push -u origin     # First push (sets upstream)
git push                       # Subsequent pushes
git pull                       # Fetch + merge
```

## 8. BRANCHING
```bash
git branch                    # List branches (* = current)
git switch -c     # Create + switch to branch
git merge             # Merge branch into current
git rebase            # Reapply commits on top of branch
```

## 9. TAGGING RELEASES
```bash
git tag                      # List tags
git tag -a  -m "" # Create annotated tag (v1.0, v2.1.3)
git push origin    # Push single tag
git push --tags              # Push all tags
```

## 10. SSH SETUP (ONE-TIME)
```bash
ssh-keygen -o                # Generate SSH key
cat ~/.ssh/id_rsa.pub        # Copy key
# Add to GitHub/GitLab: Settings → SSH Keys
```

***

### UNIVERSAL PLACEHOLDERS:
| Placeholder      | Description                                  |
|------------------|----------------------------------------------|
| ``         | Filename (FirstCode.txt, script.js, etc.)    |
| ``| Descriptive message ("Fix login bug", "Add auth") |
| ``  | Branch name (main, dev, feature/login)        |
| ``     | Tag name (v1.0.1, release-2024)              |
| ``     | https://github.com/user/repo.git              |
| ``   | git@github.com:user/repo.git                   |
| ``  | First 7 chars of commit ID (e.g., a1b2c3d)   |

***

### PRO TIPS:
1. Always `pull` before `push` to avoid conflicts  
2. `git status` is your best friend - run it often!  
3. Use `.gitignore` for files to exclude (logs, env files)  
4. VS Code's Git Graph extension visualizes branches

***

*This cheatsheet is designed for daily use to speed up your Git workflow and boost productivity.*

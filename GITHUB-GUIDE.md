# GitHub Publishing Guide

Quick guide to publish your AI Agent Learning repository to GitHub.

## 📋 Prerequisites

1. GitHub account created
2. Git installed on your Mac
3. Repository files set up locally in `~/ai-agent-learning/`

## 🚀 First Time Setup

### 1. Initialize Git Repository

```bash
cd ~/ai-agent-learning

# Initialize git
git init

# Add GitHub files
cp /path/to/downloaded/.gitignore .
cp /path/to/downloaded/README.md .
cp /path/to/downloaded/LICENSE .

# Stage all files
git add .

# Make first commit
git commit -m "Initial commit: AI Agent Learning Curriculum"
```

### 2. Create GitHub Repository

Go to [GitHub](https://github.com) and:
1. Click the `+` icon → "New repository"
2. Name: `ai-agent-learning` (or whatever you prefer)
3. Description: "Comprehensive AI Agent development curriculum for .NET developers"
4. **Make it Public** (so others can fork and learn!)
5. **Do NOT** initialize with README (you already have one)
6. Click "Create repository"

**Note:** `.gitignore` is configured to prevent API keys and secrets from being committed.

### 3. Link Local to GitHub

GitHub will show you commands. Use these:

```bash
# Add GitHub as remote
git remote add origin https://github.com/YOUR-USERNAME/ai-agent-learning.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

## 🔄 Regular Updates

After making changes to your curriculum or projects:

```bash
cd ~/ai-agent-learning

# Check what changed
git status

# Stage changes
git add .

# Commit with message
git commit -m "Description of what you changed"

# Push to GitHub
git push
```

## 📝 Example Workflow

### Completed Phase 1
```bash
git add AI-Agent-Learning-Curriculum.md
git commit -m "Completed Phase 1 - Fundamentals"
git push
```

### Added Simple Agent Code
```bash
git add projects/simple-agent/
git commit -m "Completed Simple Agent project (Phase 2.2)"
git push
```

### Updated Curriculum
```bash
git add AI-Agent-Learning-Curriculum.md
git commit -m "Updated teaching approach for RAG section"
git push
```

## 🔐 Important: Protecting Secrets

The `.gitignore` file prevents you from accidentally committing:
- API keys
- User secrets
- Build outputs
- Personal notes

**Always verify before committing:**
```bash
git status
```

Make sure no sensitive files are listed!

## 🌿 Branches (Optional)

If you want to experiment without affecting main:

```bash
# Create and switch to new branch
git checkout -b experiment

# Make changes, commit them
git add .
git commit -m "Trying new approach"

# Switch back to main
git checkout main

# If experiment worked, merge it
git merge experiment

# Delete experiment branch
git branch -d experiment
```

## 👥 Collaborating (If Sharing with Others)

### Give Access
In GitHub:
1. Go to your repository
2. Settings → Collaborators
3. Add people by username

### They Clone It
```bash
git clone https://github.com/YOUR-USERNAME/ai-agent-learning.git
cd ai-agent-learning
```

### They Can Contribute
```bash
# Make changes
git add .
git commit -m "Their changes"
git push
```

## 🆘 Common Issues

### "Permission denied"
Use HTTPS instead of SSH, or set up SSH keys:
```bash
git remote set-url origin https://github.com/YOUR-USERNAME/ai-agent-learning.git
```

### "Failed to push"
Someone else pushed first. Pull their changes:
```bash
git pull
# Resolve any conflicts
git push
```

### "Untracked files"
This is normal! Check `.gitignore` if you want to exclude them:
```bash
echo "filename" >> .gitignore
git add .gitignore
git commit -m "Updated gitignore"
```

## 📊 Viewing Your Repository

After pushing, visit:
```
https://github.com/YOUR-USERNAME/ai-agent-learning
```

You'll see:
- README.md displayed as front page
- All your files and folders
- Commit history
- Your progress!

## 🎯 Quick Reference

```bash
# Check status
git status

# Stage all changes
git add .

# Commit
git commit -m "Message"

# Push to GitHub
git push

# Pull from GitHub
git pull

# View commit history
git log --oneline

# Undo last commit (keeps changes)
git reset --soft HEAD~1
```

## 🔗 Useful Links

- [GitHub Documentation](https://docs.github.com)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Git Visual Guide](https://marklodato.github.io/visual-git-guide/index-en.html)

---

**You're ready to publish!** 🎉

Start with the "First Time Setup" section above.

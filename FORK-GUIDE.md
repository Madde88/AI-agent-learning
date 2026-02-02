# How to Fork and Use This Curriculum

Simple guide for getting started with the AI Agent Learning Curriculum.

## 🍴 Step 1: Fork the Repository

1. Go to https://github.com/ORIGINAL-USERNAME/ai-agent-learning
2. Click the **Fork** button at the top right
3. This creates YOUR copy at: `https://github.com/YOUR-USERNAME/ai-agent-learning`

**Why fork?**
- You get your own copy to work in
- You can commit your progress
- Your API keys stay in YOUR repo
- You can customize as needed

---

## 💻 Step 2: Clone Your Fork

```bash
# Clone to your computer
git clone https://github.com/YOUR-USERNAME/ai-agent-learning.git
cd ai-agent-learning

# Run setup
chmod +x setup.sh
./setup.sh
```

This creates the folder structure:
```
~/ai-agent-learning/
├── AI-Agent-Learning-Curriculum.md
└── projects/
    ├── simple-agent/
    ├── calculator-agent/
    └── ...
```

---

## 🚀 Step 3: Start Learning!

### Phase 1 (Theory)
Open **Claude Desktop App** and say:
```
"Read ~/ai-agent-learning/AI-Agent-Learning-Curriculum.md
I'm starting Phase 1, Section 1.1 - Large Language Models.
Teach me according to the curriculum."
```

### Phase 2+ (Coding)
When you reach Phase 2.2:
```bash
cd ~/ai-agent-learning/projects/simple-agent
claude code
```

In Claude Code:
```
"Read CLAUDE.md and guide me through this project."
```

---

## 📝 Step 4: Track Your Progress

### Commit Your Progress
```bash
cd ~/ai-agent-learning

# After completing a section
git add AI-Agent-Learning-Curriculum.md
git commit -m "Completed Phase 1.1 - LLM Fundamentals"
git push
```

### View Your Progress on GitHub
Go to `https://github.com/YOUR-USERNAME/ai-agent-learning`

You'll see:
- Your commits and progress
- Checkboxes in markdown files
- Your journey through the curriculum

---

## 🔐 Important: Protecting Your API Keys

The `.gitignore` file prevents you from committing:
- API keys
- User secrets
- Build outputs
- Personal notes

**But always double-check before pushing:**
```bash
git status  # See what will be committed
```

If you see files like `appsettings.Development.json` or files with "secret" in the name - **DO NOT COMMIT THEM!**

---

## 💡 Tips

### Keep Your Fork Updated
If the original curriculum is updated:
```bash
# Add original as upstream (one-time)
git remote add upstream https://github.com/ORIGINAL-USERNAME/ai-agent-learning.git

# Get latest changes
git fetch upstream
git merge upstream/main
git push
```

### Share Your Implementations?
You can choose to:
- **Keep private:** Only commit curriculum progress (checkboxes)
- **Share publicly:** Commit your code implementations too
- **Mixed:** Keep main work private, share capstone project

Edit `.gitignore` to control what gets committed.

### Want to Share Your Capstone?
When you complete Phase 4.3:
1. Make sure no secrets are in your code
2. Commit your capstone project
3. Open an issue on the original repo: "Capstone Showcase: [Your Project Name]"
4. Get featured in the Hall of Fame! 🏆

---

## 🆘 Troubleshooting

### "Claude doesn't read the curriculum"
Make sure you specify the full path:
```
"Read ~/ai-agent-learning/AI-Agent-Learning-Curriculum.md"
```

### "Claude Code doesn't see CLAUDE.md"
Claude Code automatically reads `CLAUDE.md` in the current directory. Verify:
```bash
pwd  # Should be in project folder
ls CLAUDE.md  # Should exist
```

### "I accidentally pushed an API key!"
1. **Immediately** revoke the key (OpenAI/Anthropic dashboard)
2. Remove from history: `git filter-branch` or use BFG Repo-Cleaner
3. Generate new key
4. Add to `.gitignore` to prevent future accidents

### "Merge conflicts when updating from upstream"
```bash
# Stash your changes
git stash

# Pull upstream
git fetch upstream
git merge upstream/main

# Restore your changes
git stash pop

# Resolve conflicts manually
# Then commit
```

---

## 🎓 Learning Path

1. ✅ Fork repository
2. ✅ Clone locally
3. 📚 Phase 1: Theory (1-2 weeks)
4. 💻 Phase 2: First Agent (3-5 weeks)
5. 🚀 Phase 3: Advanced (6-8 weeks)
6. 🏭 Phase 4: Production (9-12+ weeks)
7. 🎉 Share Capstone Project!

---

## 🤝 Want to Contribute?

Found a typo? Better explanation? Additional quiz questions?

Open a PR on the **original repository**, not your fork!

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

**Ready to start your AI Agent learning journey?** 🚀

Fork, clone, and dive in! The AI teacher (Claude) is waiting for you in Phase 1.1.

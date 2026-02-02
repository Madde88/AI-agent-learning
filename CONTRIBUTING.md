# Contributing to AI Agent Learning Curriculum

Thank you for considering contributing to this project! 🎉

This curriculum is designed to help .NET developers learn AI agent development, and your contributions help make it better for everyone.

## 🎯 What We're Looking For

### Content Improvements
- Clarifying explanations
- Better analogies or examples
- Additional quiz questions
- More detailed teaching instructions
- Updated references to latest packages/docs

### Project Enhancements
- Additional project variations
- Alternative approaches
- Enhanced CLAUDE.md files
- Better success criteria

### Technical Updates
- Updated package versions
- New framework recommendations (e.g., newer Semantic Kernel features)
- Performance improvements
- Bug fixes

### Community Contributions
- Sharing capstone projects
- Case studies from using the curriculum
- Translations
- Additional resources and references

## 📝 How to Contribute

### 1. Fork the Repository
Click the "Fork" button at the top right of the repository page.

### 2. Clone Your Fork
```bash
git clone https://github.com/YOUR-USERNAME/ai-agent-learning.git
cd ai-agent-learning
```

### 3. Create a Branch
```bash
git checkout -b feature/your-improvement
```

Use descriptive branch names:
- `feature/add-rag-quiz-questions`
- `fix/update-broken-link`
- `docs/clarify-phase1-instructions`

### 4. Make Your Changes

**For Curriculum Changes:**
- Edit `AI-Agent-Learning-Curriculum.md`
- Keep the teaching format consistent
- Maintain the voice (instructing an AI teacher, not the student)

**For Project Context:**
- Edit relevant `projects/*/CLAUDE.md` files
- Ensure instructions are clear for Claude Code
- Test that changes work in practice

**For Documentation:**
- Update README.md, SETUP-README.md, or GITHUB-GUIDE.md
- Keep formatting consistent
- Check links work

### 5. Test Your Changes

**For Curriculum Updates:**
- Verify markdown syntax is correct
- Check that checkboxes render properly
- Ensure references/links work

**For Code Examples:**
- If adding C# code examples, verify they compile
- Check for modern C# patterns (.NET 8+)
- Ensure async/await is used correctly

### 6. Commit Your Changes
```bash
git add .
git commit -m "Add: improved RAG section quiz questions"
```

**Commit Message Format:**
- `Add:` for new content
- `Fix:` for corrections
- `Update:` for modifications
- `Docs:` for documentation changes

Examples:
- `Add: three scenario-based questions to Phase 1.4`
- `Fix: broken link to Microsoft Agent Framework`
- `Update: Anthropic SDK references to v1.0`
- `Docs: clarify setup instructions for macOS`

### 7. Push to Your Fork
```bash
git push origin feature/your-improvement
```

### 8. Open a Pull Request

Go to the original repository and click "New Pull Request".

**In your PR description, include:**
- What you changed and why
- Any relevant context
- Screenshots if applicable (for docs changes)

## ✅ Contribution Checklist

Before submitting your PR:

- [ ] Changes are focused (one improvement per PR)
- [ ] Markdown syntax is valid
- [ ] Links are working
- [ ] Commit messages are clear
- [ ] No sensitive information (API keys, etc.)
- [ ] Consistent with existing style/format
- [ ] Teaching voice maintained (for curriculum)
- [ ] Tested changes if applicable

## 🚫 What NOT to Contribute

- Personal API keys or secrets
- Student-specific implementations (keep projects generic)
- Major restructuring without discussion first
- Promotional content or ads
- Off-topic content

## 💬 Discussion First?

For major changes, open an issue first to discuss:
- Major curriculum restructuring
- New phases or sections
- Significant changes to teaching approach
- Adding new dependencies

This ensures your work aligns with the project goals and avoids wasted effort.

## 🎓 Teaching Voice Guidelines

When contributing to the curriculum:

**✅ DO:**
- Write for the AI teacher (Claude Desktop/Code), not the student
- Use phrases like "Guide student through...", "Explain to student..."
- Include specific teaching instructions
- Provide concrete quiz questions
- Specify success criteria

**❌ DON'T:**
- Write instructions for the student (they read CLAUDE.md, not the curriculum)
- Include complete code implementations (that's the teacher's job)
- Assume student knowledge without basis
- Use imperative to student ("You should...")

**Example - Good:**
```markdown
**Teaching Approach:**
Explain RAG using the "open book exam" analogy. Guide student to understand
that RAG retrieves information at runtime rather than memorizing everything.

**Verification:**
Give quiz with 5 questions about RAG vs fine-tuning tradeoffs.
```

**Example - Bad:**
```markdown
**You will learn:**
RAG is like an open book exam. You should understand the difference
between RAG and fine-tuning.
```

## 🏆 Recognition

Contributors will be:
- Listed in the repository contributors page (automatic)
- Thanked in release notes for significant contributions
- Eligible for Hall of Fame if completing capstone project

## 📜 Code of Conduct

- Be respectful and constructive
- Welcome newcomers
- Focus on what's best for learners
- Give credit where due
- Stay on topic

## 📧 Questions?

- Open an issue for questions about contributing
- Use discussions for general questions
- Tag maintainers if you need guidance

## 🙏 Thank You!

Every contribution, no matter how small, makes this curriculum better for everyone learning AI agent development.

Happy contributing! 🚀

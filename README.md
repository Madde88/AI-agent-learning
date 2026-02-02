# AI Agent Learning Curriculum 🤖

> **A comprehensive, open-source curriculum for learning AI agent development from fundamentals to production deployment.**

Designed for experienced .NET developers who want to master building AI agents in C#. This is a complete teaching curriculum that uses Claude (via Desktop App & Code) as your AI instructor.

**🌟 Free and open-source** - Fork it, use it, contribute to it!

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

## 📚 What Is This?

This is a **complete teaching curriculum** for AI instructors (Claude Desktop App & Claude Code) to guide you through learning AI agent development. Unlike traditional courses, this uses AI as your teacher - adapting explanations to your questions and providing C# code examples on demand.

**Duration:** 6-12 months  
**Language:** C#/.NET 8+  
**Cost:** $200-500 in API costs (OpenAI/Anthropic)  
**Target:** Senior .NET developers  
**Format:** Self-paced, AI-taught

## 🍴 Why Fork This?

This curriculum is **designed to be forked**! Here's why:

- ✅ **Complete teaching system** - AI instructor + structured curriculum + projects
- ✅ **Self-paced** - Work at your own speed, 100% async
- ✅ **Proven path** - Takes you from concepts to production-ready agents
- ✅ **C#/.NET native** - All examples in modern C# with best practices
- ✅ **Free** - Only pay for API usage ($200-500 over 6-12 months)
- ✅ **Adaptable** - AI teacher adapts to YOUR questions and learning style

### Perfect For:
- Senior .NET developers wanting to learn AI agents
- Teams wanting to upskill on AI agent development
- Developers who prefer AI-taught over video courses
- Anyone who wants hands-on, project-based learning

## 🎯 What You'll Learn

### Phase 1: Fundamentals (1-2 weeks)
- How LLMs work (tokens, context, inference)
- LLMs vs Agents
- Prompts, context, and memory
- RAG (Retrieval-Augmented Generation)
- Tool use and function calling

### Phase 2: Basic Agent Building (3-5 weeks)
- Build your first agent from scratch
- Tool registry and implementation
- Agent loop patterns
- **Project:** Calculator Agent

### Phase 3: Advanced Patterns (6-8 weeks)
- RAG implementation with vector databases
- Multi-agent systems and orchestration
- Error handling and resilience (Polly)
- Observability and logging (Serilog)
- **Project:** GitHub Issue Agent

### Phase 4: Production & Specialization (9-12+ weeks)
- Production deployment (Docker, CI/CD)
- Choose specialization track
- **Capstone Project:** Your own production agent

## 📁 Repository Structure

```
ai-agent-learning/
├── AI-Agent-Learning-Curriculum.md    # Main teaching guide
├── README.md                           # This file
├── SETUP-README.md                     # Detailed setup instructions
├── setup.sh                            # Automated setup script
├── .gitignore                          # Git ignore rules
└── projects/
    ├── simple-agent/
    │   └── CLAUDE.md                   # Phase 2.2 context
    ├── calculator-agent/
    │   └── CLAUDE.md                   # Phase 2.5 context
    ├── rag-demo/
    │   └── CLAUDE.md                   # Phase 3.1 context
    ├── research-assistant/
    │   └── CLAUDE.md                   # Phase 3.2 context
    ├── github-issue-agent/
    │   └── CLAUDE.md                   # Phase 3.5 context
    └── capstone-project/
        └── CLAUDE.md                   # Phase 4.3 context
```

## 🚀 Quick Start

> **New to forking?** See [FORK-GUIDE.md](FORK-GUIDE.md) for a complete beginner-friendly guide.

### 1. Fork This Repository
Click the **Fork** button at the top right of this page to create your own copy.

### 2. Clone Your Fork
```bash
git clone https://github.com/YOUR-USERNAME/ai-agent-learning.git
cd ai-agent-learning
```

### 3. Run Setup
```bash
chmod +x setup.sh
./setup.sh
```

### 4. Start Learning

**Phase 1 (Theory)** - Open Claude Desktop App:
```
"Read ~/ai-agent-learning/AI-Agent-Learning-Curriculum.md
I'm starting Phase 1, Section 1.1.
Teach me according to the curriculum."
```

**Phase 2+ (Coding)** - Use Claude Code:
```bash
cd ~/ai-agent-learning/projects/simple-agent
claude code
```
Then say: `"Read CLAUDE.md and guide me through this project"`

## 🎓 How It Works

### For Theory (Phase 1)
- Use **Claude Desktop App**
- Claude reads the main curriculum
- Follows teaching instructions
- Explains concepts with examples
- Gives quizzes to verify understanding

### For Practice (Phase 2-4)
- Use **Claude Code** for hands-on coding
- Each project has `CLAUDE.md` with context
- Claude Code reads it and guides implementation
- You build production-quality agents in C#

## 🛠️ Prerequisites

### Required
- .NET 8 SDK or later
- C# development experience
- Basic understanding of async/await
- API keys (OpenAI and/or Anthropic)

### Helpful
- Familiarity with Clean Architecture
- Experience with dependency injection
- Testing experience (xUnit)

## 💡 Key Features

- **Concept-First:** Deep understanding before implementation
- **Hands-On:** 6 major projects from simple to complex
- **Production-Ready:** Error handling, logging, testing, deployment
- **C#/.NET Native:** All examples in modern C# with best practices
- **AI-Taught:** Curriculum designed for AI instructors to teach dynamically

## 🔧 Technologies Used

- **SDKs:** Anthropic C# SDK, OpenAI .NET SDK
- **Frameworks:** Microsoft Agent Framework, Semantic Kernel
- **RAG:** Kernel Memory, Qdrant
- **Resilience:** Polly
- **Logging:** Serilog
- **CLI:** Spectre.Console
- **Testing:** xUnit, Moq, FluentAssertions

## 📊 Progress Tracking

Each section has checkboxes:
- [ ] Theory sections (in main curriculum)
- [ ] Implementation checkpoints (in project CLAUDE.md files)

Mark them as you complete to track your progress.

## 🤝 Contributing

**Contributions are welcome!** This is a community resource.

### Ways to Contribute:

**Found an issue?**
- Open an issue describing the problem
- Suggest improvements to teaching approach
- Report broken links or outdated information

**Want to improve it?**
- Fix typos or clarify explanations
- Add additional resources or references
- Improve C# code examples
- Enhance project descriptions

**Built something cool?**
- Share your capstone project
- Write about your learning experience
- Create additional project ideas

**How to contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit with clear messages (`git commit -m 'Add: improved RAG explanation'`)
5. Push to your fork (`git push origin feature/improvement`)
6. Open a Pull Request

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

### 💡 Ideas for Contributions:
- Additional quiz questions
- More project variations
- Translations to other languages
- Python/JavaScript versions
- Additional specialization tracks
- Real-world case studies

## 📖 Documentation

- **SETUP-README.md** - Detailed setup guide
- **AI-Agent-Learning-Curriculum.md** - Complete teaching curriculum
- **Project CLAUDE.md files** - Context for each coding project

## 🎯 Success Criteria

By the end of this curriculum, you will be able to:
- ✅ Build AI agents from scratch in C#
- ✅ Implement RAG systems with vector databases
- ✅ Design and orchestrate multi-agent systems
- ✅ Deploy production-ready agents with proper error handling
- ✅ Choose and implement specialized agent patterns

## 🌟 Example Projects

### Calculator Agent (Phase 2.5)
Multi-operation calculator with beautiful CLI and comprehensive tests

### GitHub Issue Agent (Phase 3.5)
Multi-agent system that analyzes GitHub issues and creates implementation plans

### Your Capstone (Phase 4.3)
Build something real that solves an actual problem!

## 👥 Community & Support

- **Questions?** Open a [GitHub Issue](../../issues)
- **Share Progress** Use the [Discussions](../../discussions) tab
- **Show & Tell** Share your capstone projects!
- **Connect** Star ⭐ the repo to stay updated

### Hall of Fame 🏆
Completed the curriculum? Share your capstone project and we'll feature it here!

## 📚 Additional Resources

- [Anthropic Documentation](https://docs.anthropic.com)
- [Microsoft Agent Framework](https://github.com/microsoft/agents)
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel)
- [Kernel Memory](https://github.com/microsoft/kernel-memory)

## ⚖️ License

MIT License - See [LICENSE](LICENSE) file for details

This curriculum is free to use, fork, and modify. Just maintain attribution.

## 📜 Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold this code.

## 🙏 Acknowledgments

Built with:
- Anthropic Claude (teaching and content creation)
- Microsoft .NET ecosystem
- Open-source AI tooling community

---

**Ready to become an AI Agent Developer?** 🚀

Start with Phase 1 and follow the journey from fundamentals to production!

**Questions?** Open an issue or check SETUP-README.md for detailed instructions.

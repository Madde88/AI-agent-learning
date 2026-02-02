# Calculator Agent Project
## AI Agent Learning Curriculum - Phase 2.5

**Curriculum Reference:** `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md`  
**Current Section:** Phase 2.5 - Mini-Project: Calculator Agent

---

## Project Goal

Build a complete calculator agent with:
- 6+ math operations (add, subtract, multiply, divide, power, factorial)
- Complex expression handling: "(5 + 3) * 2 - 4"
- Beautiful CLI interface with colors (Spectre.Console)
- Comprehensive unit tests (>80% coverage)
- Full documentation (README)

This is the **Phase 2 capstone project** - demonstrates all Phase 2 learnings.

---

## Student Profile

- Senior .NET developer (20+ years experience)
- C#/.NET 8+
- Experienced with: Clean Architecture, SOLID, async/await, DI
- Testing: xUnit, Moq, FluentAssertions

---

## Checkpoints

- [ ] 2.5.1 6+ math operations implemented as tools
- [ ] 2.5.2 Complex expressions work: "(5 + 3) * 2 - 4"
- [ ] 2.5.3 CLI interface with colors (Spectre.Console)
- [ ] 2.5.4 Unit tests passing (>80% coverage)
- [ ] 2.5.5 Error handling for edge cases (division by zero, etc.)
- [ ] 2.5.6 README with usage examples written

---

## Current Status

**Starting fresh** - Building on Simple Agent learnings

---

## Instructions for Claude Code

You are teaching Phase 2.5 from the AI Agent Learning Curriculum.

**Read the main curriculum file** at `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md` and follow the teaching approach for section 2.5.

**Key teaching points:**
- Build on student's Simple Agent from Phase 2.2
- Create separate tool classes for each operation
- Use NCalc or similar for safe expression parsing
- Implement beautiful CLI with Spectre.Console
- Guide through comprehensive test writing (xUnit)
- Emphasize error handling and edge cases

**Project structure guidance:**
```
CalculatorAgent/
├── CalculatorAgent.csproj
├── Program.cs
├── Agents/
│   └── CalculatorAgent.cs
├── Tools/
│   ├── AddTool.cs
│   ├── SubtractTool.cs
│   ├── MultiplyTool.cs
│   ├── DivideTool.cs
│   ├── PowerTool.cs
│   └── FactorialTool.cs
└── Tests/
    └── CalculatorAgentTests.cs
```

**Success criteria:**
- All operations work correctly
- Complex expressions parsed and executed step-by-step
- CLI is attractive and user-friendly
- Tests pass with >80% coverage
- Edge cases handled gracefully
- README is clear and complete

Mark checkboxes as student completes each requirement.

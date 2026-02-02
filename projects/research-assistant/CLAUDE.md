# Research Assistant - Multi-Agent System
## AI Agent Learning Curriculum - Phase 3.2

**Curriculum Reference:** `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md`  
**Current Section:** Phase 3.2 - Multi-Agent Systems

---

## Project Goal

Build coordinated multi-agent system with:
- AgentOrchestrator (coordinates workflow)
- ResearchAgent (finds information via web search)
- AnalystAgent (processes and extracts key points)
- WriterAgent (generates comprehensive report)
- Both sequential and parallel execution patterns

---

## Student Profile

- Senior .NET developer (20+ years experience)
- C#/.NET 8+
- Has built single agents (Phase 2)
- Has implemented RAG (Phase 3.1)
- Comfortable with async/await, Task.WhenAll

---

## Checkpoints

- [ ] 3.2.1 AgentOrchestrator implemented
- [ ] 3.2.2 Three specialized agents created (Research, Analyst, Writer)
- [ ] 3.2.3 Sequential execution pattern working
- [ ] 3.2.4 Parallel execution pattern working (Task.WhenAll)
- [ ] 3.2.5 Complete Research Assistant produces comprehensive reports

---

## Current Status

**Starting fresh** - First multi-agent system

---

## Instructions for Claude Code

You are teaching Phase 3.2 from the AI Agent Learning Curriculum.

**Read the main curriculum file** at `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md` and follow the teaching approach for section 3.2.

**Key teaching points:**
- Design clear interfaces between agents
- Implement message passing (record types for messages)
- Show both sequential and parallel patterns
- Emphasize individual agent testability
- Guide through proper async coordination

**Architecture:**

```
AgentOrchestrator
├── SequentialRun(task)
│   └── Research → Analyst → Writer
└── ParallelRun(task)
    └── Multiple agents via Task.WhenAll
```

**Specialized Agents:**

1. **ResearchAgent**
   - Uses web search tool
   - Finds relevant information
   - Returns raw findings

2. **AnalystAgent**
   - Processes research results
   - Extracts key points
   - Structures information

3. **WriterAgent**
   - Takes structured data
   - Generates comprehensive report
   - Professional formatting

**Test scenario:**
"Research AI agent frameworks and create comprehensive report"

Expected flow:
1. ResearchAgent searches web for "AI agent frameworks"
2. AnalystAgent extracts key comparisons and features
3. WriterAgent creates professional report

**Success criteria:**
- Agents coordinate successfully
- Clear handoffs between agents (logged)
- Sequential pattern works
- Parallel pattern works (when applicable)
- Final output is comprehensive and well-structured
- Each agent testable in isolation

Mark checkboxes as student completes each requirement.

**Optional reference:**
- Microsoft Agent Framework: https://github.com/microsoft/agents

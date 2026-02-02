# GitHub Issue Agent
## AI Agent Learning Curriculum - Phase 3.5

**Curriculum Reference:** `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md`  
**Current Section:** Phase 3.5 - Major Project: GitHub Issue Agent

---

## Project Goal

Build production-quality multi-agent system for GitHub issue processing:
- **AnalystAgent**: Analyzes GitHub issues
- **DeveloperAgent**: Creates implementation plans
- **TesterAgent**: Designs test strategies
- **Orchestrator**: Coordinates the workflow
- **RAG Integration**: Uses project context
- **Guardrails**: Safety mechanisms (no commits to main, cost limits, approval gates)

This is the **Phase 3 capstone project** - demonstrates all Phase 3 learnings.

---

## Student Profile

- Senior .NET developer (20+ years experience)
- C#/.NET 8+
- Has completed: Simple agents, RAG, multi-agent systems
- Has implemented: Error handling (Polly), logging (Serilog)
- Ready for production-quality code

---

## Checkpoints

- [ ] 3.5.1 GitHub API integration (Octokit.NET)
- [ ] 3.5.2 All specialized agents implemented
- [ ] 3.5.3 RAG for project context
- [ ] 3.5.4 Comprehensive logging (Serilog)
- [ ] 3.5.5 Guardrails: approval gates, cost limits, safety checks
- [ ] 3.5.6 Full test coverage

---

## Current Status

**Starting fresh** - Most complex project yet

---

## Instructions for Claude Code

You are teaching Phase 3.5 from the AI Agent Learning Curriculum.

**Read the main curriculum file** at `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md` and follow the teaching approach for section 3.5.

**Key teaching points:**
- This combines ALL Phase 3 learnings
- Emphasize production quality and safety
- Guide through Octokit.NET setup
- Implement proper guardrails
- Full observability with Serilog

**Required NuGet Packages:**
- Octokit
- Polly (resilience)
- Serilog (logging)
- xUnit, Moq (testing)

**System Architecture:**

```
Orchestrator
├── AnalystAgent
│   └── Analyzes issue requirements
├── DeveloperAgent
│   └── Creates implementation plan
│   └── Uses RAG for project context
├── TesterAgent
│   └── Designs test strategy
└── Guardrails
    ├── No commits to main branch
    ├── Cost limit checks
    └── Approval gates for destructive operations
```

**GitHub API Tools:**

```csharp
// Tools needed:
- list_issues(owner, repo)
- get_issue(owner, repo, issueNumber)
- comment_on_issue(owner, repo, issueNumber, comment)
```

**Guardrails Implementation:**

```csharp
public class GitHubAgentGuardrails
{
    - CheckBranchProtection(branch)
    - CheckCostLimit(currentCost)
    - RequireApproval(operation)
}
```

**Workflow:**

1. Fetch GitHub issue
2. AnalystAgent analyzes requirements
3. DeveloperAgent creates plan (using RAG for context)
4. TesterAgent designs tests
5. Generate comprehensive report
6. (Optional) Post comment to issue

**Safety First:**
- Never commit to main
- Always require approval for posting
- Track costs
- Comprehensive logging
- Rate limiting (Polly)

**Success criteria:**
- Processes real GitHub issues successfully
- Generates useful, actionable analysis
- All guardrails work correctly
- Production-quality code
- Full test coverage
- Comprehensive logging shows all decisions

**Test with:**
- Small bug fix issues
- Documentation updates
- Simple feature requests
- Use test repository first!

Mark checkboxes as student completes each requirement.

**References:**
- Octokit.NET: https://github.com/octokit/octokit.net

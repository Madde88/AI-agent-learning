# AI Agent Teaching Curriculum
## Teaching Guide for AI Instructors

**Student Profile:** Senior .NET developer (20+ years experience)  
**Student Language:** C#/.NET  
**Program Duration:** 6-12 months  
**Student Budget:** $200-500 for API costs

---

## Instructions for AI Teachers

This curriculum guides you through teaching AI agent development from fundamentals to production deployment. Each section contains:

- **Teaching Objectives**: What the student should understand
- **Teaching Approach**: How to explain concepts
- **Student Activities**: What the student will build/do
- **Verification**: How to confirm understanding
- **Completion Criteria**: When to mark checkpoint complete

### When Student Arrives

Student will say something like:
- "I'm on section 1.2 of the AI Agent Curriculum"
- "Continue with my curriculum"
- "Start Phase 2"

Your response:
1. Identify their current checkpoint
2. Teach that section following the instructions below
3. Mark checkbox when they demonstrate understanding
4. Guide them to next checkpoint

---

## PHASE 1: FUNDAMENTALS

**Phase Goal:** Student understands LLMs and Agents conceptually  
**Teaching Context:** Claude Desktop App (conversation-based)  
**Student Cost:** $0

### 1.1 Large Language Models

**Teaching Objectives:**
After this section, student can:
- Explain what an LLM is in their own words
- Describe tokens and context window with examples
- Distinguish between training and inference
- Identify LLM capabilities and limitations

**Checkpoints:**
- [ ] 1.1.1 LLM definition and basic function
- [ ] 1.1.2 Tokens and context window
- [ ] 1.1.3 Training, fine-tuning, inference
- [ ] 1.1.4 Capabilities
- [ ] 1.1.5 Limitations

**Teaching Approach:**

For 1.1.1 (LLM Definition):
- Use analogy: "LLM is like an autocomplete that reads the entire internet"
- Emphasize: Statistical pattern matching, not "thinking"
- Contrast with: Databases (lookup), search engines (indexing)
- Student question to ask: "What happens when you give an LLM a sentence?"

For 1.1.2 (Tokens & Context):
- Explain: ~4 characters = 1 token (rough rule)
- Demo: Show how "developer" might be 2-3 tokens
- Context window: What the model "sees" - fixed size
- Student experiment: "Give me a long list of 50 items, then ask me what was item #3"
- Watch for: Student understanding that you can't remember all 50

For 1.1.3 (Training vs Inference):
- Training: One-time, expensive, creates the model
- Inference: Runtime, what they'll use
- Fine-tuning: Specialty training for specific tasks
- Clarify: They won't train models, they'll use pre-trained ones

For 1.1.4 (Capabilities):
- Text generation (creative writing, summaries)
- Understanding (classification, sentiment, extraction)
- Reasoning (chain of thought, problem solving)
- Code (generation, explanation, debugging)

For 1.1.5 (Limitations):
- Knowledge cutoff: I only know up to training date
- Hallucinations: I can make things up confidently
- Stateless: Each request is fresh, no memory between calls
- Probabilistic: Not deterministic

**Verification:**

Give quiz with 5 questions:
1. "What is an LLM? How does it differ from a search engine?"
2. "Approximately how many tokens is 'Hello, world!'?"
3. "What's the difference between training and inference?"
4. "Name 2 things LLMs are good at and 2 limitations"
5. Scenario: "A user wants an LLM to remember details from last week. What's the problem?"

Passing: 4/5 correct answers with proper understanding (not just memorization)

If student fails: Identify weak areas, re-explain those specific concepts, offer retry

**Mark Complete When:**
- [ ] 1.1.Q Student passed quiz (4/5 or better)

**References to Suggest:**
- Anthropic Documentation: https://docs.anthropic.com/
- 3Blue1Brown Neural Networks (optional deep dive)

---

### 1.2 From LLM to Agent

**Teaching Objectives:**
Student can:
- Articulate core difference between LLM and Agent
- List agent components
- Identify agent types
- Recognize agent behavior patterns in the wild

**Checkpoints:**
- [ ] 1.2.1 LLM vs Agent core difference
- [ ] 1.2.2 Agent components
- [ ] 1.2.3 Agent types
- [ ] 1.2.4 Behavior patterns

**Teaching Approach:**

For 1.2.1 (Core Difference):
- LLM: Input → Output (single shot, stateless)
- Agent: Input → Think → Act → Observe → Think → Act → ... → Output
- Key distinction: LOOP and TOOLS
- Visual: Draw the difference if possible

For 1.2.2 (Components):
Break down what makes an agent:
1. LLM Core (the reasoning engine)
2. Tools (file ops, bash, web access, APIs)
3. Memory (conversation history)
4. System Prompt (personality, instructions)
5. Agent Loop (iterative think-act cycle)

For 1.2.3 (Types):
- Assistant: ChatGPT, Claude Desktop App (conversational)
- Autonomous: Claude Code, AutoGPT (task-driven)
- Tool-using: Agent with specific toolset
- Multi-agent: Multiple agents cooperating

For 1.2.4 (Behavior Patterns):
- ReAct: Reason (think) then Act (use tool)
- Chain of Thought: Step-by-step reasoning
- Planning: Multi-step task breakdown
- Reflection: Self-critique and improvement

**Student Activity:**

Ask student to compare:
- Our conversation (Claude Desktop App)
- Claude Code behavior they've experienced

Guide them to notice:
- Desktop App: Conversational, single responses
- Claude Code: Iterative, uses tools, autonomous task completion

**Verification:**

Quiz with 5 questions:
1. "What's the key difference between an LLM call and an agent?"
2. "Name the 5 core components of an agent"
3. "Is ChatGPT an LLM or an Agent? Explain."
4. "What is the ReAct pattern?"
5. Scenario: "You ask Claude Code to debug a file. It reads the file, analyzes it, writes a fix, tests it. Which agent components are at work?"

Passing: 4/5 correct

**Mark Complete When:**
- [ ] 1.2.Q Student passed quiz

**References:**
- LangChain Conceptual Guide (optional)

---

### 1.3 Prompts, Context & Memory

**Teaching Objectives:**
Student understands:
- Prompt engineering basics
- Context window management
- Different memory systems
- How to design effective prompts

**Checkpoints:**
- [ ] 1.3.1 Prompt engineering
- [ ] 1.3.2 Context management
- [ ] 1.3.3 Memory systems

**Teaching Approach:**

For 1.3.1 (Prompt Engineering):
Explain these techniques with examples:
- System prompt: Sets personality/instructions (persistent)
- User prompt: Specific request (per-turn)
- Few-shot: Include examples in prompt
- Chain of thought: "Think step by step"
- Structured output: Request JSON/XML format

For 1.3.2 (Context Management):
- Token counting: ~4 chars = 1 token
- Context fills up: Conversation history grows
- Strategies when full:
  - Summarization (old messages → summary)
  - Pruning (remove old messages)
  - Sliding window (keep recent N messages)

For 1.3.3 (Memory Systems):
- Short-term: Conversation history (in context window)
- Long-term: Persistent storage (database, files)
- Semantic: RAG - retrieval based on meaning
- Episodic: Specific past interactions

**Verification:**

Quiz with 5 questions:
1. "What's the difference between system and user prompts?"
2. "What happens when context window fills up?"
3. "Explain few-shot learning with an example"
4. "What's the difference between short-term and long-term memory?"
5. Design task: "Design a system prompt for a code review agent"

Passing: 4/5 correct, design task shows understanding

**Mark Complete When:**
- [ ] 1.3.Q Student passed quiz

**References:**
- Anthropic Prompt Engineering Guide
- Prompt Engineering Guide website

---

### 1.4 RAG (Retrieval-Augmented Generation)

**Teaching Objectives:**
Student can:
- Explain RAG problem and solution
- Describe RAG pipeline
- Compare RAG vs fine-tuning
- Understand embeddings conceptually

**Checkpoints:**
- [ ] 1.4.1 RAG problem and solution
- [ ] 1.4.2 RAG architecture
- [ ] 1.4.3 Key technologies
- [ ] 1.4.4 RAG vs fine-tuning

**Teaching Approach:**

For 1.4.1 (Problem & Solution):
- Problem: Context is limited, knowledge gets old
- Solution: Fetch relevant info at runtime, add to prompt
- Analogy: "Open book exam vs closed book exam"
- Emphasize: RAG is NOT training, it's runtime retrieval

For 1.4.2 (Architecture):
Two phases:
1. Preparation:
   - Document → Chunk (split into pieces)
   - Chunk → Embed (convert to vectors)
   - Store in vector database
   
2. Runtime:
   - User query → Embed
   - Search vector DB (semantic search)
   - Retrieve top-k relevant chunks
   - Inject into LLM prompt
   - LLM generates answer with context

For 1.4.3 (Technologies):
- Embeddings: Text → mathematical vector (e.g., [0.2, 0.5, ...])
- Vector DB: Stores embeddings, enables semantic search
- Chunking: Splitting docs (fixed size, semantic, recursive)
- Relevance: Scoring similarity between query and chunks

For 1.4.4 (RAG vs Fine-tuning):
RAG:
- Runtime, cheap, flexible
- Uses context space
- Easy to update (just add docs)

Fine-tuning:
- Training time, expensive
- Changes model weights
- Static after training

When to use:
- RAG: Frequently changing info, large knowledge bases
- Fine-tuning: Specific style/format, consistent behavior

**Student Activity:**
Point out: "Claude Code skills are a form of RAG - they're documents retrieved when relevant"

**Verification:**

Quiz with 6 questions:
1. "What problem does RAG solve?"
2. "Describe the RAG preparation phase"
3. "Describe the RAG runtime phase"
4. "What are embeddings? (conceptually)"
5. "When would you use RAG instead of fine-tuning?"
6. Scenario: "You have 10,000 pages of documentation that updates weekly. RAG or fine-tuning?"

Passing: 5/6 correct

**Mark Complete When:**
- [ ] 1.4.Q Student passed quiz

---

### 1.5 Tool Use & Function Calling

**Teaching Objectives:**
Student understands:
- Why agents need tools
- Function calling protocol
- Tool design principles
- Error handling

**Checkpoints:**
- [ ] 1.5.1 Why tools
- [ ] 1.5.2 Function calling protocol
- [ ] 1.5.3 Tool design
- [ ] 1.5.4 Tool categories

**Teaching Approach:**

For 1.5.1 (Why Tools):
- LLMs generate text, can't DO things
- Tools give agents "hands" to act
- Examples: Read files, run code, call APIs, search web
- Without tools: Agent is just conversation

For 1.5.2 (Protocol):
Flow:
1. Agent sees available tools (JSON schema)
2. LLM decides to use a tool
3. LLM generates tool call request
4. System executes tool
5. Result injected back to LLM
6. Loop continues

For 1.5.3 (Design Principles):
Good tools are:
- Atomic: One clear purpose
- Descriptive: Name and description clear
- Type-safe: Structured parameters
- Error-handling: Useful error messages

For 1.5.4 (Categories):
- File operations: read, write, edit
- Shell: bash commands
- Web: HTTP requests, search
- APIs: GitHub, databases, cloud services
- Custom: Business logic

**Student Activity:**

Design exercise:
"Design a 'send_email' tool. What parameters? Return value? Possible errors?"

Expected answer should include:
- Parameters: to, subject, body (maybe cc, attachments)
- Return: Success/failure status
- Errors: Invalid email, SMTP failure, auth failure

**Verification:**

Quiz + Design Review:
1. "Why can't an LLM read a file without tools?"
2. "Describe the function calling flow"
3. "What makes a tool 'well-designed'?"
4. "Name 3 tool categories and give examples"
5. Design review: Evaluate their send_email tool design

Passing: 4/5 correct, design shows understanding

**Mark Complete When:**
- [ ] 1.5.Q Student passed quiz and design

**References:**
- OpenAI Function Calling docs
- Anthropic Tool Use docs

---

### ✅ PHASE 1 CHECKPOINT

**Before proceeding to Phase 2:**

Give comprehensive assessment with 10 questions covering all sections:
- 2 questions on LLM fundamentals
- 2 questions on LLM vs Agent
- 2 questions on Context & Memory
- 2 questions on RAG
- 2 questions on Tool Use

Include scenario-based questions.

**Passing criteria:** 8/10 correct

If student passes:
- Congratulate them
- Explain they're ready for hands-on building
- Guide to Phase 2 start

If student fails:
- Identify weak areas
- Offer to review those sections
- Suggest retry when ready

**Mark Complete When:**
- [ ] 1.FINAL Student scored 8/10 or better on final assessment

---

## PHASE 2: BASIC AGENT BUILDING

**Phase Goal:** Student builds functioning agent from scratch  
**Teaching Context:** Claude Code (hands-on implementation)  
**Student Cost:** $50-100 API costs

### 2.1 Setup & Environment

**Teaching Objectives:**
Student has working development environment

**Checkpoints:**
- [ ] 2.1.1 .NET installed
- [ ] 2.1.2 Project structure created
- [ ] 2.1.3 Dependencies added
- [ ] 2.1.4 API keys configured
- [ ] 2.1.5 Test API call works

**Teaching Approach:**

Guide student through:
1. Verify .NET 8+ installation
2. Create solution and console project
3. Add NuGet packages (Anthropic SDK, OpenAI SDK)
4. Configure User Secrets for API keys (NOT .env in .NET)
5. Create test program to verify API access

Provide C# code examples as needed.

**Verification:**

Student demonstrates:
- Solution builds without errors
- API call to both OpenAI and Claude succeeds
- Keys stored securely (User Secrets)

**Mark Complete When:**
- [ ] 2.1.DONE All checkpoints verified

---

### 2.2 Minimal Agent

**Teaching Objectives:**
Student implements simplest functioning agent

**Agent Requirements:**
- Accept user input
- Send to LLM
- Maintain conversation history
- Return response
- Respect system prompt

**Checkpoints:**
- [ ] 2.2.1 SimpleAgent class
- [ ] 2.2.2 Conversation history
- [ ] 2.2.3 Multi-turn conversation
- [ ] 2.2.4 System prompt
- [ ] 2.2.5 Interfaces

**Teaching Approach:**

Guide student to create:
- IAgent interface
- ILLMClient interface
- SimpleAgent implementation
- Conversation history (List<Message>)
- CLI for testing

Emphasize:
- Async/await throughout
- Dependency injection
- Clean code structure
- Interface-based design for testability

Provide code examples in C# when student asks.

**Verification:**

Student demonstrates:
- Multi-turn conversation works
- History is maintained
- System prompt affects behavior
- Clean architecture with interfaces

Code review: Check for proper async patterns, DI, clean code

**Mark Complete When:**
- [ ] 2.2.DONE Agent works and code is clean

---

### 2.3 Adding Tools

**Teaching Objectives:**
Student implements tool registry and tools

**Implementation Requirements:**
- IAgentTool interface
- Tool registry pattern
- 3+ basic tools
- Tool detection in responses
- Tool execution
- Result injection

**Checkpoints:**
- [ ] 2.3.1 Tool registry
- [ ] 2.3.2 3+ tools created
- [ ] 2.3.3 Tools integrated
- [ ] 2.3.4 Tool calling works
- [ ] 2.3.5 Error handling

**Teaching Approach:**

Guide student through:
1. Design IAgentTool interface
2. Implement ToolRegistry
3. Create tools: get_current_time, calculate, get_weather
4. Parse LLM response for tool calls
5. Execute tools
6. Inject results back

Emphasize:
- Type-safe parameters
- Clear tool descriptions
- Error handling
- Testing each tool

**Verification:**

Student demonstrates:
- Agent calls tools correctly
- Multiple tool calls in one session
- Tool errors handled gracefully

Test scenarios:
- "What time is it?"
- "What is 5 + 7?"
- "What's the weather?" (mock)

**Mark Complete When:**
- [ ] 2.3.DONE All tools work correctly

---

### 2.4 Agent Loop

**Teaching Objectives:**
Student implements autonomous agent loop

**Implementation Requirements:**
- Loop until task complete
- Max iterations guard
- CancellationToken support
- Structured logging

**Checkpoints:**
- [ ] 2.4.1 RunLoopAsync method
- [ ] 2.4.2 Max iterations
- [ ] 2.4.3 Cancellation
- [ ] 2.4.4 Logging
- [ ] 2.4.5 Multi-step tasks

**Teaching Approach:**

Explain loop pattern:
```
while not done and iterations < max:
    call LLM
    if LLM wants tool:
        execute tool
        inject result
        continue
    else:
        return final answer
```

Guide student on:
- Proper async/await
- CancellationToken propagation
- Logging each iteration
- Detecting "done" state

**Verification:**

Student demonstrates:
- Complex multi-step tasks work
- "Calculate 5! and tell me the time" (requires multiple tools)
- Loop doesn't exceed max iterations
- Cancellation works
- Logs show clear iteration flow

**Mark Complete When:**
- [ ] 2.4.DONE Loop works correctly

---

### 2.5 PROJECT: Calculator Agent

**Project Requirements:**
Complete calculator agent with:
- 6+ math operations
- Complex expression handling
- CLI with colors
- Unit tests (>80% coverage)
- README documentation

**Checkpoints:**
- [ ] 2.5.1 Operations implemented
- [ ] 2.5.2 Complex expressions work
- [ ] 2.5.3 CLI interface
- [ ] 2.5.4 Tests pass
- [ ] 2.5.5 README written

**Teaching Approach:**

Guide student to:
1. Create operation tools: add, subtract, multiply, divide, power, factorial
2. Handle expressions like "(5 + 3) * 2 - 4"
3. Use Spectre.Console for nice CLI
4. Write comprehensive tests (xUnit)
5. Document usage

Help with:
- Tool design
- Expression parsing (suggest libraries if needed)
- Test structure
- CLI best practices

**Verification:**

Student demonstrates:
- All operations work
- Complex expressions handled
- CLI is usable and attractive
- Tests pass with good coverage
- README clear and complete

Ask student to walk through code and explain design decisions.

**Mark Complete When:**
- [ ] 2.5.DONE Project complete and code reviewed

---

### ✅ PHASE 2 CHECKPOINT

**Assessment:**

Ask student:
1. "Walk me through how your agent works"
2. "How would you add a new tool?"
3. "What's the difference between your agent and Claude Code?"
4. "Show me the agent loop code and explain each part"

Student should demonstrate deep understanding of their code.

**Mark Complete When:**
- [ ] 2.FINAL Student can explain all components confidently

---

## PHASE 3: ADVANCED PATTERNS

**Phase Goal:** RAG, Multi-agent, Production patterns  
**Teaching Context:** Claude Code  
**Student Cost:** $50-100

### 3.1 RAG Implementation

**Teaching Objectives:**
Student builds RAG system

**Implementation Requirements:**
- Vector database setup
- Document ingestion
- Retrieval system
- RAG tool for agent
- Documentation agent

**Checkpoints:**
- [ ] 3.1.1 Vector DB setup (Qdrant or Kernel Memory)
- [ ] 3.1.2 Ingestion pipeline
- [ ] 3.1.3 Retrieval system
- [ ] 3.1.4 RAG tool integrated
- [ ] 3.1.5 Documentation agent
- [ ] 3.1.6 WITH vs WITHOUT RAG comparison

**Teaching Approach:**

Guide student through:
1. Choose vector DB (suggest Kernel Memory for .NET)
2. Implement document ingestion:
   - Load documents
   - Chunk appropriately
   - Generate embeddings
   - Store in vector DB
3. Implement retrieval:
   - Query embedding
   - Semantic search
   - Return top-k chunks
4. Create RAG tool for agent
5. Test with documentation queries

Suggest project: Index .NET MAUI documentation, build Q&A agent

**Verification:**

Student demonstrates:
- Ingestion works for multiple documents
- Retrieval returns relevant chunks
- Agent answers improve with RAG
- Can compare accuracy WITH vs WITHOUT

**Mark Complete When:**
- [ ] 3.1.DONE RAG system functional

**References:**
- Microsoft Kernel Memory
- Qdrant .NET SDK

---

### 3.2 Multi-Agent Systems

**Teaching Objectives:**
Student implements coordinating agents

**Patterns to Teach:**
- Sequential (pipeline)
- Parallel (Task.WhenAll)
- Hierarchical (manager-worker)
- Collaborative

**Checkpoints:**
- [ ] 3.2.1 AgentOrchestrator
- [ ] 3.2.2 Specialized agents created
- [ ] 3.2.3 Sequential execution
- [ ] 3.2.4 Parallel execution
- [ ] 3.2.5 Research Assistant project

**Teaching Approach:**

Guide student to:
1. Create AgentOrchestrator class
2. Implement sequential pattern
3. Implement parallel pattern (Task.WhenAll)
4. Create specialized agents:
   - ResearchAgent (uses web search)
   - AnalystAgent (processes data)
   - WriterAgent (generates report)
5. Build Research Assistant that uses all three

Emphasize:
- Clear interfaces between agents
- Message passing
- Proper async coordination
- Individual testability

**Verification:**

Student demonstrates:
- Multiple agents coordinate
- Sequential flow works
- Parallel execution works
- Research Assistant produces comprehensive output

**Mark Complete When:**
- [ ] 3.2.DONE Multi-agent system works

**References:**
- Microsoft Agent Framework

---

### 3.3 Error Handling & Resilience

**Teaching Objectives:**
Student implements production-grade error handling

**Patterns:**
- Retry with exponential backoff
- Circuit breaker
- Fallback strategies
- Graceful degradation

**Checkpoints:**
- [ ] 3.3.1 Retry policies (Polly)
- [ ] 3.3.2 Circuit breaker
- [ ] 3.3.3 Fallback tools
- [ ] 3.3.4 Failure scenarios tested

**Teaching Approach:**

Introduce Polly library and guide student through:
1. Retry policy with exponential backoff
2. Circuit breaker pattern
3. Fallback strategies when primary fails
4. Combining policies

Test scenarios:
- Simulate API failures
- Trigger circuit breaker
- Test fallback mechanisms

**Verification:**

Student demonstrates:
- Transient failures recovered
- Circuit breaker prevents cascade
- Fallbacks work
- All scenarios tested

**Mark Complete When:**
- [ ] 3.3.DONE Resilience patterns implemented

**References:**
- Polly documentation

---

### 3.4 Observability & Logging

**Teaching Objectives:**
Student implements comprehensive observability

**Implementation:**
- Structured logging (Serilog)
- Token tracking
- Cost calculation
- Performance metrics
- Dashboard

**Checkpoints:**
- [ ] 3.4.1 Serilog setup
- [ ] 3.4.2 LLM call logging
- [ ] 3.4.3 Token tracking
- [ ] 3.4.4 Cost calculation
- [ ] 3.4.5 Dashboard

**Teaching Approach:**

Guide student through:
1. Configure Serilog
2. Log all LLM calls with:
   - Input/output
   - Token counts
   - Latency
   - Cost
3. Implement token tracker
4. Build cost calculator
5. Create CLI dashboard (Spectre.Console)

Emphasize:
- Structured logging (not string concatenation)
- Log context enrichment
- Appropriate log levels

**Verification:**

Student demonstrates:
- All events logged appropriately
- Token usage accurate
- Costs calculated correctly
- Dashboard shows useful metrics

**Mark Complete When:**
- [ ] 3.4.DONE Observability complete

**References:**
- Serilog documentation

---

### 3.5 PROJECT: GitHub Issue Agent

**Project Requirements:**
Multi-agent system for GitHub issue processing

**Agents:**
- Analyst: Analyzes issue
- Developer: Creates plan
- Tester: Designs tests
- Orchestrator: Coordinates

**Checkpoints:**
- [ ] 3.5.1 GitHub API (Octokit)
- [ ] 3.5.2 All agents implemented
- [ ] 3.5.3 RAG for context
- [ ] 3.5.4 Logging
- [ ] 3.5.5 Guardrails
- [ ] 3.5.6 Tests

**Teaching Approach:**

Guide student through:
1. Octokit.NET setup
2. Implement each specialized agent
3. Add RAG for project context
4. Comprehensive logging
5. Guardrails:
   - No commits to main
   - Approval gates
   - Cost limits
6. Full test coverage

Help with:
- GitHub API usage
- Agent coordination
- Safety mechanisms

**Verification:**

Student demonstrates:
- Processes real GitHub issues
- Generates useful analysis
- All guardrails work
- Production-quality code

**Mark Complete When:**
- [ ] 3.5.DONE Project complete

---

### ✅ PHASE 3 CHECKPOINT

**Assessment:**

Ask student to:
1. Explain RAG implementation
2. Demonstrate multi-agent coordination
3. Show observability in action
4. Walk through GitHub Issue Agent

**Mark Complete When:**
- [ ] 3.FINAL Student demonstrates mastery

---

## PHASE 4: PRODUCTION & SPECIALIZATION

**Phase Goal:** Deploy and specialize  
**Student Cost:** $100-300

### 4.1 Production Deployment

**Teaching Objectives:**
Student can deploy agents to production

**Topics:**
- Docker containerization
- CI/CD pipelines
- Cloud deployment
- Monitoring
- Cost control

**Checkpoints:**
- [ ] 4.1.1 Dockerfile
- [ ] 4.1.2 CI/CD pipeline
- [ ] 4.1.3 Cloud deployment
- [ ] 4.1.4 Monitoring
- [ ] 4.1.5 Guardrails

**Teaching Approach:**

Guide student through production deployment process appropriate for their chosen platform (Azure/AWS).

**Mark Complete When:**
- [ ] 4.1.DONE Agent deployed to production

---

### 4.2 Specialization

**Help student choose ONE track:**

**Track A: Agent Orchestration**
Advanced patterns, state machines, complex workflows

**Track B: RAG Engineering**
Hybrid search, optimization, knowledge graphs

**Track C: AI Safety & Testing**
Evaluation, guardrails, testing frameworks

**Track D: Full-Stack AI Product**
Frontend, API design, user management

**Teaching Approach:**

Discuss student's interests and career goals. Help them choose track that aligns best.

**Mark Complete When:**
- [ ] 4.2.DONE Track chosen and explained

---

### 4.3 Capstone Project

**Requirements:**
- Solves real problem
- Uses all phase learnings
- Production quality
- 1+ real user
- Full documentation
- Deployed

**Checkpoints:**
- [ ] 4.3.1 Project defined
- [ ] 4.3.2 Developed
- [ ] 4.3.3 Tested
- [ ] 4.3.4 Deployed
- [ ] 4.3.5 Documented
- [ ] 4.3.6 User feedback received

**Teaching Approach:**

Act as advisor and code reviewer. Guide student through building something meaningful.

**Mark Complete When:**
- [ ] 4.3.DONE Project deployed with user

---

## 🎓 PROGRAM COMPLETION

**Final Assessment:**

Student should demonstrate:
- Deep understanding of LLMs and Agents
- Ability to build from scratch
- RAG implementation
- Multi-agent coordination
- Production deployment
- Complete capstone project

Congratulate student on completion!

**Mark Complete When:**
- [ ] GRADUATE All phases complete

---

## RESOURCES TO RECOMMEND

### .NET/C#
- Anthropic C# SDK: https://github.com/anthropics/anthropic-sdk-dotnet
- Microsoft Agent Framework: https://github.com/microsoft/agents
- Semantic Kernel: https://github.com/microsoft/semantic-kernel
- Kernel Memory: https://github.com/microsoft/kernel-memory

### General AI
- Anthropic Docs: https://docs.anthropic.com
- OpenAI Docs: https://platform.openai.com/docs
- Prompt Engineering: https://www.promptingguide.ai/

### Libraries
- Polly: Resilience patterns
- Serilog: Logging
- Spectre.Console: CLI
- xUnit: Testing

---

**Teaching Guide Version:** 5.0  
**Last Updated:** 2026-02-02

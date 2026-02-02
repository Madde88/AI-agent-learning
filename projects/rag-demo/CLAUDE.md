# RAG Demo Project
## AI Agent Learning Curriculum - Phase 3.1

**Curriculum Reference:** `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md`  
**Current Section:** Phase 3.1 - RAG Implementation

---

## Project Goal

Build RAG (Retrieval-Augmented Generation) system from scratch:
- Document ingestion pipeline
- Vector database (Qdrant or Kernel Memory)
- Semantic search and retrieval
- RAG-powered agent for documentation Q&A
- Compare WITH vs WITHOUT RAG

---

## Student Profile

- Senior .NET developer (20+ years experience)
- C#/.NET 8+
- Has completed Phase 2 (built agents from scratch)
- Understands RAG conceptually from Phase 1.4

---

## Checkpoints

- [ ] 3.1.1 Vector database setup (Qdrant or Kernel Memory)
- [ ] 3.1.2 Document ingestion pipeline working
- [ ] 3.1.3 Retrieval system functional
- [ ] 3.1.4 RAG tool integrated into agent
- [ ] 3.1.5 Documentation Agent built (suggest: .NET MAUI docs)
- [ ] 3.1.6 Comparison demo: WITH vs WITHOUT RAG

---

## Current Status

**Starting fresh** - First RAG implementation

---

## Instructions for Claude Code

You are teaching Phase 3.1 from the AI Agent Learning Curriculum.

**Read the main curriculum file** at `~/ai-agent-learning/AI-Agent-Learning-Curriculum.md` and follow the teaching approach for section 3.1.

**Key teaching points:**
- Recommend **Kernel Memory** (Microsoft) for .NET integration
- Alternative: Qdrant .NET client if student prefers
- Guide through two-phase architecture:
  1. Preparation: Document → Chunk → Embed → Store
  2. Runtime: Query → Embed → Search → Retrieve → Inject
- Create RAG tool that agent can use
- Emphasize chunking strategies
- Test with .NET MAUI or other technical documentation

**Suggested packages:**
- Microsoft.KernelMemory.Core
- Microsoft.KernelMemory.MemoryStorage.Qdrant
- OR Qdrant.Client

**Project focus:**
Build a "Documentation Assistant" that:
1. Ingests technical documentation
2. Answers questions using RAG
3. Shows clear improvement over non-RAG answers

**Success criteria:**
- Documents successfully ingested and chunked
- Semantic search returns relevant chunks
- Agent provides better answers with RAG
- Clear demonstration of WITH vs WITHOUT RAG
- Citations/sources included in answers

Mark checkboxes as student completes each requirement.

**References to suggest:**
- Microsoft Kernel Memory: https://github.com/microsoft/kernel-memory
- Qdrant .NET: https://github.com/qdrant/qdrant-dotnet

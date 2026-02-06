# notebook-creator

Create new Jupyter notebooks following repository standards and best practices.

**When to use:**
- Creating new example notebooks from scratch
- Building tutorials or how-to guides
- Demonstrating Pinecone features or integrations
- Need a well-structured notebook template

## What This Command Does

Creates production-ready Jupyter notebooks that follow all repository standards with:
- Proper structure and organization
- SDK v8+ syntax
- Clear, educational content
- Working code examples
- Installation shields and badges
- Resource cleanup

## Creation Process

1. **Research Phase**
   - Review `.ai/notebook-standards.md` for structure requirements
   - Review `.ai/writing-guidelines.md` for style guidelines
   - Check existing similar notebooks for patterns
   - Research latest Pinecone SDK documentation

2. **Notebook Structure**
   - Clear title and introduction
   - Installation/setup section with shields (Colab, nbviewer)
   - Prerequisite requirements (API keys, dependencies)
   - Logical sections with markdown explanations
   - Code cells with clear, commented examples
   - Resource cleanup section at the end

3. **Code Standards**
   - Pinecone SDK v8+ syntax
   - Environment variables for API keys (never hardcoded)
   - Error handling with informative messages
   - Clear variable names
   - Python best practices (PEP 8)

4. **Content Requirements**
   - Clear, concise explanations in markdown
   - Working code that demonstrates concepts
   - Expected outputs shown in cells
   - Links to relevant Pinecone documentation
   - Troubleshooting tips where appropriate

## Example Usage

```
Create a new notebook showing semantic search with Pinecone
Build a notebook demonstrating RAG with Cohere embeddings
I need a notebook for hybrid search with metadata filtering
Create an example showing how to use Pinecone with LangChain
```

---

*For Claude Code users: This command maps to the `notebook-creator` agent in `.claude/agents/`*

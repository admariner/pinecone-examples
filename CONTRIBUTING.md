# Contributing to Pinecone Examples

We appreciate your contributions to help us improve and maintain this community resource!

## Quick Contributions

For quick fixes like correcting a typo or patching an obvious bug, feel free to open a pull request directly.

## Larger Changes

If you're considering a larger or more involved change to this repository, its organization, or the functionality of one of the examples, please first [open a new issue](https://github.com/pinecone-io/examples/issues/new) and describe your proposed changes so we can discuss them together before you invest a ton of time or effort into making changes.

## Development Setup

This repository uses [uv](https://docs.astral.sh/uv/) for fast Python package management.

1. Install dependencies:
   ```bash
   uv sync
   ```

2. Install pre-commit hooks:
   ```bash
   uv run pre-commit install
   ```

The hooks will automatically format and lint your code when you commit.

### Running Checks Manually

```bash
# Lint a file
uv run ruff check path/to/file.py

# Format a file
uv run ruff format path/to/file.py
```

## Notebook Guidelines

- Ensure the notebook runs cleanly with "Restart Kernel and Run All"
- Include cleanup cells at the end to delete any indexes created
- Follow standards in `.ai/notebook-standards.md`
- See `.ai/quality-checklist.md` for final quality checks
- Review `.ai/writing-guidelines.md` for style and voice

## Working with AI

This repository includes specialized AI agents and skills to help with common tasks. Both Claude Code and Cursor users can leverage these tools.

### Quick Skills

Use these slash command skills for common tasks:

```bash
/validate-notebook path/to/notebook.ipynb    # Check notebook quality
/review-notebook-writing path/to/notebook.ipynb  # Review writing style
/update-notebook-shields path/to/notebook.ipynb  # Add/update badges
```

### Specialized Agents

We have 5 specialized agents for complex workflows. Simply describe what you need in natural language, and the appropriate agent will help.

#### For Claude Code Users

Agents are in `.claude/agents/` and trigger automatically:

```bash
# Review a notebook
"Review the semantic-search.ipynb notebook for quality issues"

# Create a new notebook
"Create a notebook showing RAG with Cohere embeddings"

# Test examples
"Test all notebooks in learn/search/ for errors"

# Update documentation
"Fix all broken links in the README files"

# Migrate to new SDK
"Migrate integrations/openai/ examples to SDK v8"
```

#### For Cursor Users

Commands are in `.cursor/commands/` - use natural language to invoke:

```bash
# Review a notebook
"Use notebook-reviewer to check semantic-search.ipynb"

# Create a new notebook
"Use notebook-creator to build a hybrid search example"

# Test examples
"Use pinecone-tester on the RAG notebook"

# Update documentation
"Use docs-updater to validate all links"

# Migrate to new SDK
"Use example-migrator to update deprecated patterns"
```

### Available Agents

| Agent | Purpose | Location |
|-------|---------|----------|
| **notebook-reviewer** | Review notebooks against quality standards | `.claude/agents/` `.cursor/commands/` |
| **notebook-creator** | Create new notebooks following best practices | `.claude/agents/` `.cursor/commands/` |
| **pinecone-tester** | Test Pinecone integrations and validate SDK usage | `.claude/agents/` `.cursor/commands/` |
| **docs-updater** | Update documentation and maintain consistency | `.claude/agents/` `.cursor/commands/` |
| **example-migrator** | Migrate examples to newer SDK versions | `.claude/agents/` `.cursor/commands/` |

Each agent has full access to repository standards in `.ai/` and provides detailed, context-aware assistance.

See `AGENTS.md` for complete specifications of what each agent does.

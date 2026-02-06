# Jupyter Notebook Standards

Comprehensive requirements for Jupyter notebooks in the Pinecone examples repository.

## Structure

### Required Sections

**First cell (markdown):**
- Brief introduction explaining what the notebook demonstrates
- 1-2 paragraphs setting context

**Prerequisites section:**
- Required packages and versions
- API keys needed
- Background knowledge assumptions

**Clear section headers:**
- Group related cells logically
- Use consistent heading levels
- Guide reader through the workflow

**Summary or next steps (when appropriate):**
- Recap key learnings
- Suggest related examples or resources

**Single focus:**
- Keep notebooks focused on one topic or workflow
- Avoid combining multiple unrelated concepts

### Cell Organization

**First code cell:**
- Group ALL imports in the first code cell
- Exception: Conditional imports that depend on earlier logic
- Use consistent import order (standard library, third-party, local)

**Cell focus:**
- Keep each cell focused on a single concept or step
- Avoid overly long cells—break them up with markdown explanations

**Variable naming:**
- Don't reuse variable names for different purposes across cells
- Use descriptive names that persist clearly through the notebook

## Code Quality

### Readability

- Write clear, readable code that prioritizes understanding over cleverness
- Follow Python best practices and PEP 8 style guidelines
- Use meaningful variable names that reflect the domain (e.g., `query_embedding` not `x`)
- Use named keyword arguments instead of positional arguments
- Add comments to explain the "why" when the code alone isn't self-explanatory

### Documentation

- All helper functions and classes should have clear docstrings explaining their purpose
- Keep docstrings concise but complete

### Error Handling

- Include error handling where appropriate to demonstrate production-ready patterns
- Show how to handle common failure cases
- Use try/except blocks judiciously (not for flow control)

## Dependencies and Versions

### Pinning Requirements

**All dependencies must be pinned with exact versions:**
```python
%pip install -qU pinecone==5.0.0 openai==1.12.0
```

**Never use unpinned dependencies:**
```python
# ❌ BAD
%pip install pinecone openai

# ❌ BAD
%pip install pinecone>=5.0.0

# ✅ GOOD
%pip install pinecone==5.0.0 openai==1.12.0
```

**Why:** Ensures reproducibility and prevents breakage from unexpected version changes.

### API Keys and Secrets

**Never hardcode secrets:**
```python
# ❌ BAD
api_key = "sk-proj-abc123..."
```

**Use environment variables with getpass fallback:**
```python
# ✅ GOOD
import os
from getpass import getpass

api_key = os.environ.get("PINECONE_API_KEY") or getpass("Enter your Pinecone API key: ")
```

## Documentation

### Markdown Cells

**Explain the "why" before code:**
- Markdown cells should provide context and explain the reasoning behind each step
- Keep explanations concise but complete enough for someone new to the topic
- Anticipate reader questions

**Consistency:**
- Review existing notebooks in the repository to maintain consistent style and terminology
- Use the same terms for the same concepts

## Execution and Validation

### Execution Requirements

**Must run cleanly:**
- Ensure the notebook runs cleanly with "Restart Kernel and Run All"
- Cells must be executable in order from top to bottom
- Avoid cells that depend on out-of-order execution

**Markdown rendering:**
- Check that all markdown renders correctly
- Test links to ensure they're not broken

### Output

**Meaningful output:**
- Show meaningful output that illustrates the concept being taught
- Clear or truncate large outputs that add noise
- Add print statements to show intermediate results when helpful

**Progress indicators:**
- Use `tqdm` or status messages for long-running operations
- Indicate expected wait times for slow cells when helpful

## Reproducibility

### Random Seeds

- Set random seeds when using randomness
- Document the seed value used
- Helps readers reproduce exact results

### External Dependencies

- Note external dependencies clearly (API keys, data files)
- Provide sample data or clear instructions for obtaining it
- Make notebooks as self-contained as possible

## Resource Management

### Cleanup Cells

**Required for notebooks that create resources:**
- Include cleanup cells at the end to delete indexes, close connections
- Must delete any Pinecone indexes created during the notebook
- Use try/finally or context managers where appropriate

**Example cleanup cell:**
```python
# Cleanup - Delete the index
pc.delete_index("example-index")
```

### Context Managers

- Use context managers where appropriate (file handles, connections)
- Demonstrates production-ready patterns

## Validation

Notebooks are validated by:
- **Structure validation:** First cell markdown, imports grouped, cleanup cells present
- **Dependency pinning:** All packages pinned with exact versions
- **Secrets detection:** No hardcoded API keys or tokens
- **Link validation:** All markdown links are valid
- **Format validation:** Valid notebook JSON structure

Use the `validate-notebook` skill to run these checks.

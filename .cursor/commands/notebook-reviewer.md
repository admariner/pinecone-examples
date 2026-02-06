# notebook-reviewer

Review Jupyter notebooks against the repository's quality standards and writing guidelines.

**When to use:**
- Reviewing notebooks before publishing or merging PRs
- Checking standards compliance
- Validating notebook quality
- Ensuring notebooks follow best practices

## What This Command Does

Reviews notebooks against:
- `.ai/notebook-standards.md` - Technical requirements and structure
- `.ai/writing-guidelines.md` - Style, voice, and content quality
- `.ai/quality-checklist.md` - Final quality checks

## Review Process

1. **Standards Compliance Check**
   - Clear setup instructions and prerequisites
   - Proper error handling and user guidance
   - Clean cell outputs (no sensitive data)
   - Working examples with clear explanations
   - Installation shields (Colab, nbviewer badges)
   - Resource cleanup at the end

2. **Pinecone-Specific Checks**
   - Correct Pinecone SDK usage (v8+ syntax)
   - Proper API key handling (environment variables)
   - Index creation and cleanup
   - Up-to-date dependency versions with pinned versions

3. **Code Quality**
   - Consistent code style and formatting
   - Proper markdown formatting and headings
   - Links to relevant Pinecone documentation

## Output Format

Lists specific issues found with:
- Cell numbers/locations
- Actionable suggestions for improvements
- Categorized as: **Critical**, **Important**, or **Minor**
- Security concerns highlighted immediately

## Example Usage

```
Review the semantic-search.ipynb notebook for quality issues
Check if learn/search/hybrid-search.ipynb follows all guidelines
Validate all notebooks in the integrations/langchain directory
```

---

*For Claude Code users: This command maps to the `notebook-reviewer` agent in `.claude/agents/`*

# pr-open

Open a pull request on GitHub using the prepare-pr skill for comprehensive PR preparation.

**Recommended workflow:**
1. Run the prepare-pr skill to guide through the full PR preparation process
2. The skill provides a 7-step workflow covering review, validation, and PR creation

**PR Format** (if creating manually):

**Title:**
- Use format: `<type>: <brief description>`
- Types: feat, fix, docs, chore, refactor, test

**Description:**
Use the structured format from prepare-pr skill:
```markdown
## Summary
[1-3 sentences explaining what this PR does and why]

## Changes
- Bullet point list of main changes
- Focus on user-facing changes
- Mention any breaking changes

## Test Plan
- [ ] Notebook runs with "Restart Kernel and Run All"
- [ ] All validation checks pass
- [ ] Output matches expected results

## Additional Context
[Optional: Screenshots, links, related issues]
```

**Metadata:**
- Apply appropriate GitHub label (bug, enhancement, documentation, chore)
- Link to any related GitHub issues or Linear issues

If the PR addresses a Linear issue, update the ticket with a link to the GitHub PR.


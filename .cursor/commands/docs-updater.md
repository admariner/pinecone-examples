# docs-updater

Update documentation and ensure consistency across the repository.

**When to use:**
- Updating README files or markdown documentation
- Fixing broken links (404 checks)
- Updating SDK version references
- Refreshing example outputs after changes
- Maintaining documentation consistency
- After Pinecone feature releases

## What This Command Does

Maintains and updates all documentation with:
- Link validation and fixing
- Version reference updates
- Content consistency checks
- Cross-reference validation
- Style consistency enforcement

## Documentation Types

- README files (main and subdirectory)
- Markdown documentation in `/docs`
- Inline code documentation
- Contributing guidelines

## Update Process

1. **Scope Assessment**
   - Determine what needs updating
   - Identify affected files

2. **Link Validation**
   - Check external URLs with WebFetch
   - Verify internal links work correctly
   - Update or replace broken links

3. **Content Updates**
   - Update SDK version references
   - Refresh installation instructions
   - Maintain consistency across all docs
   - Ensure references to notebooks exist
   - Update tables of contents when structure changes

4. **Style Consistency**
   - Follow markdown best practices
   - Maintain consistent terminology
   - Use clear, concise language
   - Keep formatting uniform across files

5. **Pinecone-Specific Updates**
   - Track Pinecone feature releases
   - Update examples for new capabilities
   - Deprecate outdated patterns
   - Link to official Pinecone docs appropriately

## Output Format

- List of files updated
- Summary of changes made
- Any broken links found and fixed
- Consistency issues resolved
- Recommendations for additional updates

## Example Usage

```
Check and fix all broken links in the documentation
Update SDK references from v7 to v8 across all READMEs
Validate all internal cross-references in the docs
Refresh the example outputs in the main README
Update documentation after the new serverless features
```

---

*For Claude Code users: This command maps to the `docs-updater` agent in `.claude/agents/`*

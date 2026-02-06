# example-migrator

Migrate examples to newer SDK versions and update deprecated patterns.

**When to use:**
- Migrating examples to a new Pinecone SDK version
- Updating deprecated code patterns
- Modernizing examples to current best practices
- After major SDK releases
- When deprecation warnings appear

## What This Command Does

Systematically migrates Pinecone examples with:
- Identification of outdated patterns
- Research of migration guides
- Careful code updates
- Thorough testing
- Documentation updates

## Migration Process

1. **Migration Planning**
   - Identify examples using old SDK patterns
   - Review migration guides and breaking changes
   - Plan backward-compatible updates where possible
   - Test changes thoroughly

2. **Common Migration Patterns**
   - Update import statements to new SDK structure
   - Replace deprecated methods with current equivalents
   - Update index creation syntax
   - Modernize query/upsert patterns
   - Update metadata filtering syntax

3. **Testing Requirements**
   - Verify migrated code runs successfully
   - Ensure outputs are equivalent to before
   - Check for new warnings or deprecations
   - Validate against current best practices

4. **Documentation Updates**
   - Update comments explaining the changes
   - Add notes about version requirements
   - Update README or setup instructions
   - Document any breaking changes

5. **Quality Assurance**
   - Maintain code clarity and readability
   - Don't change more than necessary
   - Preserve example intent and pedagogy
   - Keep error handling robust

## Example Migrations

Common SDK v7 → v8 migrations:
- `pinecone.init()` → `from pinecone import Pinecone; pc = Pinecone()`
- `pinecone.Index()` → `pc.Index()`
- `index.upsert()` parameter changes
- Metadata filtering syntax updates

## Output Format

- List of files migrated
- Summary of changes per file
- Test results confirming functionality
- Any issues or warnings encountered
- Version compatibility notes

## Example Usage

```
Migrate the semantic-search examples to SDK v8
Update deprecated patterns in integrations/langchain/
Check learn/search/ for examples needing SDK migration
Migrate all examples using the old init() pattern
Update the hybrid-search notebook to use current SDK
```

---

*For Claude Code users: This command maps to the `example-migrator` agent in `.claude/agents/`*

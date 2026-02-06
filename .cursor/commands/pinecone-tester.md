# pinecone-tester

Test Pinecone examples and validate SDK integration code.

**When to use:**
- Testing notebooks or scripts for errors
- Validating SDK integration code
- Checking examples after SDK updates
- Verifying examples work correctly
- CI/CD troubleshooting

## What This Command Does

Executes and validates Pinecone examples with:
- Environment variable checks
- Isolated execution
- Error and warning detection
- SDK version validation
- Resource cleanup verification
- Performance assessment

## Testing Process

1. **Pre-Test Setup**
   - Check for required environment variables (PINECONE_API_KEY)
   - Verify dependencies are installed
   - Review test requirements

2. **Execution and Monitoring**
   - Execute notebooks or scripts in isolation
   - Monitor for errors, warnings, and deprecation notices
   - Validate outputs match expected results
   - Check index creation and operations
   - Verify proper cleanup (indexes deleted)

3. **SDK Version Validation**
   - Ensure examples use current SDK syntax (v8+)
   - Flag deprecated methods or patterns
   - Check for breaking changes from SDK updates

4. **Error Reporting**
   - Document any failures with full error messages
   - Provide context: which cell/line failed and why
   - Suggest fixes for common issues
   - Identify environment-specific problems

5. **Performance Checks**
   - Note any unusually slow operations
   - Flag inefficient patterns
   - Suggest optimizations where appropriate

## Output Format

Reports with:
- Test summary and status
- Environment check results
- Execution results per operation
- Issues categorized by severity (Critical/Important/Minor)
- SDK compliance report
- Resource cleanup validation
- Performance notes and recommendations

## Example Usage

```
Test the semantic-search.ipynb notebook
Validate the RAG example in learn/generation/
Check if all notebooks in integrations/openai/ are working
Run tests on the hybrid-search example
```

---

*For Claude Code users: This command maps to the `pinecone-tester` agent in `.claude/agents/`*

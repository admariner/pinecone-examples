# file-issue

Create a Linear ticket in the project Notebook Examples.

Give the ticket the following labels:
- docs:examples
- agent-ready

In the description of the ticket include the following content:

```
Repository: https://github.com/pinecone-io/examples
Target Branch: master
```


And at the end of the ticket description add these instructions:

```
When the fix is complete, the agent should:

1. **Quality Review**
   - Run validate-notebook skill: Technical validation (structure, pinning, secrets, links)
   - Run review-notebook-writing skill: Writing style, voice, tone, and clarity
   - Run check-deprecated-models skill: Check for deprecated AI models
   - Verify the notebook executes successfully from top to bottom
   - Ensure code follows Python best practices and is well-commented
   - Check that all markdown cells render correctly
   - Implement fixes for any issues uncovered.

2. **Create Pull Request**
   - Create a PR with a title that follows Conventional Commits format
   - Include a clear description of what was improved and why
   - Reference the related GitHub issue and Linear issue number
   - Summarize the user value of the improvement
   ```
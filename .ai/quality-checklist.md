# Notebook Quality Checklist

Quick reference for verifying notebook quality before publication.

## Structure ✓

- [ ] First cell is markdown with introduction
- [ ] Prerequisites section lists requirements
- [ ] Clear section headers throughout
- [ ] Cleanup section at end (if creates resources)
- [ ] Summary or next steps (when appropriate)

## Code Quality ✓

- [ ] All imports in first code cell
- [ ] Meaningful variable names (domain-specific)
- [ ] Named keyword arguments (not positional)
- [ ] Helper functions have docstrings
- [ ] PEP 8 style followed
- [ ] No deprecated APIs or patterns

## Dependencies ✓

- [ ] All packages pinned with exact versions (`package==version`)
- [ ] No hardcoded API keys or secrets
- [ ] Environment variables with getpass fallback for keys

## Documentation ✓

- [ ] Markdown explains "why" before code
- [ ] Technical terms defined on first use
- [ ] Context provided for each step
- [ ] Consistent terminology

## Writing Style ✓

- [ ] Voice consistent throughout (we/you/impersonal)
- [ ] No time references (dates, "recently", "new")
- [ ] No marketing language or superlatives
- [ ] Professional but friendly tone
- [ ] Simple, clear sentences

## Execution ✓

- [ ] Runs cleanly with "Restart Kernel and Run All"
- [ ] Cells execute in order (no out-of-order dependencies)
- [ ] All markdown renders correctly
- [ ] Links are valid

## Output ✓

- [ ] Meaningful outputs shown
- [ ] Large outputs truncated
- [ ] Progress indicators for long operations

## Resource Management ✓

- [ ] Cleanup cells delete created resources
- [ ] Context managers used where appropriate
- [ ] No orphaned resources

## Validation ✓

- [ ] Structure validation passes (`validate-notebook` skill)
- [ ] No secrets detected
- [ ] All dependencies pinned
- [ ] Links are valid

## Review ✓

- [ ] Writing quality reviewed (`review-notebook-writing` skill)
- [ ] No deprecated models (`check-deprecated-models` skill)
- [ ] Follows standards in `.ai/notebook-standards.md`
- [ ] Follows guidelines in `.ai/writing-guidelines.md`

---

For detailed standards, see:
- **`.ai/notebook-standards.md`** - Complete technical requirements
- **`.ai/writing-guidelines.md`** - Comprehensive writing guidance

For automated validation:
- **`validate-notebook` skill** - Technical validation
- **`review-notebook-writing` skill** - Writing quality review
- **`check-deprecated-models` skill** - Model availability check

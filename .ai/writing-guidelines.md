# Writing Guidelines

Comprehensive guidance for writing clear, professional, and effective documentation in Jupyter notebooks.

## Target Audience

Content in the Pinecone examples repository is written for:
- Developers comfortable with Python and APIs
- Those familiar with basic ML/AI concepts (embeddings, models, etc.) but not necessarily experts
- People looking for practical, working examples they can adapt to their own projects
- Those who may be new to vector databases specifically

## Persona and Approach

**Write as:**
- Someone with deep expertise but who explains difficult concepts without condescension
- A smart peer helping another developer solve a problem, not as a lecturer
- Someone focused on practical outcomes rather than theory

**Don't write as:**
- A marketing person promoting a product
- An academic writing a research paper
- Someone assuming expert-level knowledge

## Voice Principles

### Choose Appropriate Voice by Content Type

**Jupyter Notebook Tutorials:**
- Use first person plural ("we") for collaborative learning
- Creates sense of partnership and shared journey
- Example: "We'll create an index and upload embeddings"

**How-To Guides and Documentation:**
- Use second person ("you") for direct instructions
- Emphasizes reader agency and action
- Example: "You can configure the index with custom metadata"

**Reference Material:**
- Use impersonal/passive voice
- Focus on objective facts and behavior
- Example: "The index is created with serverless architecture"

### Consistency Within Content

- Choose one voice per document and stick with it
- Don't switch between "we", "you", and impersonal within the same section
- Exception: Impersonal voice for objective statements is acceptable even in "we" notebooks

### Company Voice

- Say "we" and "us" when referring to Pinecone as a company
- Example: "We'll use Pinecone's serverless architecture..."
- This is distinct from the tutorial "we" (you + reader)

## Tone Guidelines

### Factual and Objective

- Present information factually
- Avoid self-praise and unsupported claims
- Substantiate statements with data whenever possible
- Let the code and results speak for themselves

### Collegial and Professional

- Being factual doesn't mean being formal
- Use friendly but professional language
- Avoid overly casual language ("super cool!", "awesome!")
- Avoid overly formal language ("utilize", "leverage", "facilitate")

### Plain, Clear Explanations

- Explain concepts plainly, without being pedantic
- Use straightforward language that is easy to understand
- Define technical terms on first use
- Break complex concepts into digestible chunks

### No Flowery Language

- Avoid nebulous or decorative adjectives
- Choose precise words that convey meaning directly
- Say "fast" not "blazingly fast"
- Say "accurate" not "incredibly accurate"

## Timeless Content

### Avoid Time References

**Never use:**
- Specific dates, years, or time references (e.g., "as of 2024", "in January 2025")
- Phrases like "recently released", "coming soon", "new feature"
- "cutting-edge", "state-of-the-art", "latest"
- "This year", "last month", "currently"

**Use instead:**
- "This example demonstrates..." (not "This new feature allows...")
- "Pinecone supports..." (not "Pinecone recently added...")
- Simply describe what exists, without temporal context

### Avoid Version References in Prose

- Don't reference specific version numbers unless necessary for compatibility
- Pin versions in code, but don't mention them in explanatory text
- Exception: When discussing migration or breaking changes

**Bad:**
```markdown
Pinecone 5.0 introduced the inference API, which allows you to...
```

**Good:**
```markdown
Pinecone's inference API allows you to...
```

### Professional, Not Marketing

**Focus on what the code does:**
- Describe functionality accurately
- Explain benefits or purpose honestly, without exaggeration
- Avoid superlatives ("the best", "revolutionary", "game-changing")
- No unsubstantiated claims

**Bad:**
```markdown
Pinecone's revolutionary serverless architecture is the best solution for vector search.
```

**Good:**
```markdown
Pinecone's serverless architecture automatically scales based on usage and requires no capacity planning.
```

## Writing Style

### Simple Sentences

- Use basic subject-verb-object construction
- Avoid long appositives and dependent clauses
- Don't chain multiple dependent clauses
- One idea per sentence when possible

**Bad:**
```markdown
When using Pinecone, which is a vector database that provides fast similarity search, you can leverage the serverless architecture that automatically scales, which means you don't need to provision capacity.
```

**Good:**
```markdown
Pinecone is a vector database that provides fast similarity search. It uses serverless architecture that automatically scales based on usage. You don't need to provision capacity.
```

### Concise Structure

- Keep sentences short and to the point
- Eliminate unnecessary words and redundancies
- Remove filler words ("actually", "basically", "essentially")

### Punctuation

- Use simple punctuation
- Reserve em dashes (—) for moments of strong emphasis only
- Use colons to introduce lists or explanations
- Avoid excessive exclamation points

### Data-Driven

- Support statements with relevant data or examples when possible
- Show, don't just tell
- Use code examples to demonstrate concepts

### No Self-Adulation

- Do not use language that promotes or flatters the brand without evidence
- Focus on factual capabilities
- Let performance speak for itself

## Clarity and Readability

### Define Technical Terms

- Define jargon and technical terms on first use
- Provide context for domain-specific concepts
- Link to external resources for deep dives

**Example:**
```markdown
Vector embeddings are numerical representations of text that capture semantic meaning. For example, "king" and "queen" have similar embeddings because they're semantically related.
```

### Provide Context Before Code

- Always explain what code will do before showing it
- Explain why this approach is being used
- Preview the expected outcome

### Break Down Complex Concepts

- Split complex ideas into smaller, manageable pieces
- Use examples to illustrate abstract concepts
- Build understanding progressively

### Use Concrete Examples

- Abstract explanations benefit from concrete examples
- Show real-world use cases
- Make it relatable to the reader's experience

## Structural Guidelines

### Clear Introduction

- State what the notebook will teach
- Explain why this is useful
- Set expectations for what readers will build

### Logical Progression

- Each section should build on previous ones
- Smooth transitions between topics
- Clear narrative flow from start to finish

### Helpful Headings

- Use descriptive section headings
- Make content skimmable
- Help readers navigate the notebook

### Summary and Next Steps

- Recap key learnings at the end
- Suggest related topics or examples
- Provide resources for further learning

## What to Avoid

### Don't

- Use overly complex sentence structures
- Include vague or embellished descriptions
- Make unsubstantiated claims
- Use excessive punctuation or stylistic flourishes
- Switch voice mid-document
- Use undefined jargon
- Skip context before code examples
- End abruptly without summary

## Review Checklist

Before publishing, verify:
- [ ] Voice is consistent throughout (we/you/impersonal)
- [ ] Tone is professional but friendly
- [ ] No time-specific references (dates, "new", "recently")
- [ ] Technical terms are defined on first use
- [ ] Code has explanatory context before it
- [ ] Sentences are clear and concise
- [ ] No marketing language or superlatives
- [ ] Examples are concrete and helpful
- [ ] Structure flows logically
- [ ] Introduction sets clear expectations
- [ ] Summary reinforces key points

Use the `review-notebook-writing` skill for comprehensive writing review.

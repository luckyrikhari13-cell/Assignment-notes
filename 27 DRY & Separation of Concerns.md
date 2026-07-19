# DRY

DRY stands for Don't Repeat Yourself.

If the same logic is used in multiple places, extract it into a reusable function.

---

# Separation of Concerns

Each file should have one responsibility.

Example:

redditSearchAgent.ts
- AI pipeline

handleStream.ts
- Streaming logic

outputParser.ts
- Parsing logic
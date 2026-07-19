# Query Rewriter

## Purpose

The query rewriter converts the user's input into a cleaner query that can be used by the search step.

---

## RunnableLambda

```ts
const rewriteQuery = new RunnableLambda({
    func(input) {
        return input.query;
    }
});
```

### input

The data received by this step.

### input.query

The user's latest question.

### return

Outputs the extracted query string.

---

## Data Flow

Input object

↓

Extract query

↓

Return query string

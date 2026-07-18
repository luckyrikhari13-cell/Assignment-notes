# RunnableSequence

## What is RunnableSequence?

RunnableSequence is a LangChain class that executes multiple Runnables one after another. The output of one Runnable automatically becomes the input of the next.

---

## Why do we need it?

Without RunnableSequence, developers manually connect many function calls.

RunnableSequence makes AI pipelines easier to read, modify, and reuse.

---

## Syntax

```ts
RunnableSequence.from([
    runnable1,
    runnable2,
    runnable3
]);
```

---

## from()

A static method used to create a RunnableSequence.

### Parameter

Array<Runnable>

### Returns

RunnableSequence

---

## Execution Flow

Input

↓

Runnable 1

↓

Runnable 2

↓

Runnable 3

↓

Output

---

## Important Points

- Executes sequentially.
- Every element must be a Runnable.
- RunnableSequence itself is also a Runnable.
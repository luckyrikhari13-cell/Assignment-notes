# Pipe Operator

## What is pipe()?

`pipe()` is a Runnable method that connects one Runnable to another, forming a pipeline.

---

## Why do we need it?

It provides a cleaner and more readable alternative to `RunnableSequence.from()`.

---

## Syntax

```ts
const chain = prompt
    .pipe(llm)
    .pipe(new StringOutputParser());
```

---

## Parameter

`pipe(nextRunnable)`

- Accepts another Runnable.

---

## Returns

A new Runnable representing the combined pipeline.

---

## Equivalent Syntax

```ts
RunnableSequence.from([
    prompt,
    llm,
    parser
]);
```

is equivalent to

```ts
prompt
    .pipe(llm)
    .pipe(parser);
```

---

## Key Idea

- `pipe()` does not execute the chain.
- It only connects Runnables.
- Execution starts when `invoke()`, `stream()`, or another execution method is called.

---

# 🧠 My Analogy

`pipe()` is like a magnetic connector between Iron Man suit parts. Each `pipe()` joins one component to the next until the entire suit is assembled into a single working system.
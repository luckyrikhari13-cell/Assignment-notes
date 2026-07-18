# RunnableLambda

## What is RunnableLambda?

RunnableLambda is a LangChain class that wraps a normal JavaScript or TypeScript function so it can behave like a Runnable.

---

## Why do we need it?

Sometimes we need small pieces of custom logic inside a LangChain pipeline.

RunnableLambda lets us include ordinary JavaScript functions without breaking the pipeline.

---

## Syntax

```ts
const runnable = new RunnableLambda({
    func(input) {
        return input;
    }
});
```

---

## Parameters

### func

A JavaScript function that receives an input and returns an output.

---

## Returns

A Runnable that can be used inside RunnableSequence or RunnableMap.

---

## Common Uses

- Cleaning text
- Filtering arrays
- Formatting data
- Extracting object properties
- Sorting
- Mapping
- Validation

---

## Key Idea

RunnableLambda is an adapter that converts ordinary JavaScript functions into LangChain Runnables.

---

# 🧠 My Analogy

RunnableLambda is like an adapter that lets a non-standard machine connect to a factory assembly line. It wraps normal JavaScript code so it can participate in a LangChain pipeline.
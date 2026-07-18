# PromptTemplate

## What is PromptTemplate?

PromptTemplate is a LangChain class used to create prompts with placeholders that are filled with values at runtime.

---

## Why do we need it?

Instead of manually concatenating long strings, PromptTemplate keeps prompts clean, reusable, and easy to maintain.

---

## Syntax

```ts
const prompt = PromptTemplate.fromTemplate(
    "Hello {name}"
);
```

---

## Parameters

### template

A string containing placeholders such as `{name}`.

---

## Returns

A `PromptTemplate`, which is also a Runnable.

---

## invoke()

```ts
await prompt.invoke({
    name: "Lucky"
});
```

Output:

```text
Hello Lucky
```

---

## Key Idea

- Input: Object containing values.
- Output: A fully formatted prompt string.
- PromptTemplate does **not** call the LLM; it only prepares the prompt.

---

# 🧠 My Analogy

PromptTemplate is like an email template or mail merge.

You write the message once with placeholders (e.g., `{name}`), and later supply the values to generate the final personalized message.
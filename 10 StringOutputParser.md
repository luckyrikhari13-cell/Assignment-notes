# StringOutputParser

## What is StringOutputParser?

StringOutputParser is a LangChain Runnable that extracts the text content from an LLM's response.

---

## Why do we need it?

LLMs usually return structured objects containing metadata, token usage, IDs, and the generated content.

Most applications only need the generated text.

StringOutputParser extracts that text.

---

## Syntax

```ts
const parser = new StringOutputParser();
```

---

## invoke()

Input:

```ts
AIMessage {
    content: "Hello"
}
```

Output:

```text
Hello
```

---

## Key Idea

- Input: LLM response object.
- Output: Plain string.
- Does not modify the answer.
- Only extracts the text.

---

# 🧠 My Analogy

Ordering food from a restaurant:

The restaurant gives you a pizza inside a box with a receipt and napkins.

StringOutputParser opens the box and hands you only the pizza (the generated text), leaving behind the packaging (metadata).
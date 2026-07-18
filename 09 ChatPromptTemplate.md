# ChatPromptTemplate

## What is ChatPromptTemplate?

ChatPromptTemplate is a LangChain class used to create prompts for chat-based LLMs. Instead of producing one string, it produces a structured list of messages.

---

## Why do we need it?

Modern chat models (GPT, Gemini, Claude, etc.) expect conversations as a sequence of messages with roles rather than a single block of text.

---

## Syntax

```ts
const prompt = ChatPromptTemplate.fromMessages([
    ["system", "You are a helpful assistant."],
    ["user", "{question}"]
]);
```

---

## Parameters

### fromMessages()

Accepts an array of message definitions.

Each message contains:
- Role (`system`, `user`, `assistant`)
- Content (may include placeholders)

---

## invoke()

```ts
await prompt.invoke({
    question: "What is React?"
});
```

Returns a formatted chat prompt (an array of messages).

---

## Common Roles

### system
Defines the AI's behavior.

### user
Represents the user's message.

### assistant
Represents previous AI responses.

---

## Difference from PromptTemplate

PromptTemplate:
- Produces one formatted string.

ChatPromptTemplate:
- Produces a structured conversation (list of messages).

---

# 🧠 My Analogy

PromptTemplate is like writing a document.

ChatPromptTemplate is like writing a movie script, where every line is tagged with the speaker (`system`, `user`, or `assistant`).
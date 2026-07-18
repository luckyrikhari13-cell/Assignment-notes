# RunnableMap

## What is RunnableMap?

RunnableMap is a LangChain Runnable that creates a new object by computing multiple values from the same input.

---

## Why do we need it?

Many Runnables expect structured input such as:

- query
- chat_history
- context

RunnableMap prepares that object before passing it to the next Runnable.

---

## Syntax

```ts
RunnableMap.from({
  query: (input) => input.query,

  chat_history: (input) => input.chat_history,

  context: retrieverChain,
});
```

---

## Input

One object.

---

## Output

A new object containing multiple computed values.

---

## Difference from RunnableSequence

RunnableSequence

Input

↓

Step1

↓

Step2

↓

Output

RunnableMap

Input

↓

Multiple independent computations

↓

One combined object

---

## Difference from Promise.all()

Promise.all()

Returns an Array.

RunnableMap

Returns an Object.

RunnableMap works with Runnables rather than only Promises.

---

# 💡 Memory Analogy – Iron Man Suit Assembly

Think of **RunnableMap** like the **Iron Man suit assembly** in _Iron Man 2_.

Tony Stark is standing in one place (the **input**).

```
               Tony Stark (Input)
                      │
      ┌───────────────┼────────────────┐
      │               │                │
      ▼               ▼                ▼
   Helmet          Left Arm        Right Arm
      │               │                │
      ▼               ▼                ▼
   Chest Plate       Legs            Boots
      \               |              /
       \              |             /
        └─────────────┼────────────┘
                      ▼
            Complete Iron Man Suit
```

Every suit part is built and attached **independently**, but they all start from the same trigger (Tony calling the suit).

Similarly, in `RunnableMap`:

```ts
RunnableMap.from({
  query: (input) => input.query,
  chat_history: (input) => input.chat_history,
  context: retrieverChain,
});
```

Every branch receives the **same input object**.

- `query` extracts the search query.
- `chat_history` extracts the conversation history.
- `context` retrieves relevant documents.

After all branches finish, `RunnableMap` combines their outputs into **one final object**.

### Key Takeaway

RunnableMap is like Iron Man's suit assembly:

- One input (Tony Stark).
- Multiple independent parts work simultaneously.
- Everything is assembled into one complete object.

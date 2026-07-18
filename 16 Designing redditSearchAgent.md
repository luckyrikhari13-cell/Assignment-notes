# Designing redditSearchAgent

## Goal

Create an AI pipeline that answers user questions using Reddit search results.

---

## Input

- query
- chat_history

---

## Output

- Streamed AI response

---

## Pipeline

User Input

↓

Rewrite Query

↓

Search Reddit

↓

Rerank Posts

↓

Process Posts

↓

RunnableMap

↓

ChatPromptTemplate

↓

LLM

↓

StringOutputParser

↓

Streaming

---

## Key Idea

Each Runnable transforms the input into a new type of output. The pipeline is a sequence of data transformations.
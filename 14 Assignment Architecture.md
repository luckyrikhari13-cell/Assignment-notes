# Assignment Architecture

The assignment is NOT asking us to build 8 completely different AI systems.

Instead, we build one architecture and reuse it with small modifications.

There are four categories:

## Group A

Search → Rerank → Context → LLM → Stream

Agents:

- academic
- reddit
- web
- youtube

---

## Group B

Search → Filter → Return List

Agents:

- image
- video

---

## Group C

No search

Chat History

↓

LLM

↓

Stream

Agent:

- writingAssistant

---

## Group D

Chat History

↓

Prompt

↓

LLM

↓

Custom Output Parser

↓

Suggestions Array

Agent:

- suggestionGenerator

---

The assignment teaches pattern recognition rather than memorizing code.


Re-ranking is the process of reordering retrieved documents based on their similarity or relevance to the user's query so the LLM receives the most useful context first.
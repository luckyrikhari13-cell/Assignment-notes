# Assignment Overview

## Goal

Build multiple AI search/chat agents using LangChain.

The assignment provides two completed reference agents:

- academicSearchAgent
- imageSearchAgent

The remaining agents must follow the same architecture.

The project teaches how to compose AI systems using LangChain Runnables instead of writing one large function.

---

## Architecture

User

↓

Agent

↓

Prompt

↓

LLM

↓

Parser

↓

Response

Some agents also retrieve external information before generating the answer.
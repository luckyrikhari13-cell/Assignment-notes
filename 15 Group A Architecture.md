# Group A Architecture

## Goal

Generate a streamed answer using retrieved external information.

---

## Pipeline

User Query

↓

Query Rewriter (PromptTemplate + LLM)

↓

Search Engine

↓

Retrieved Documents

↓

Rerank (Embeddings + Cosine Similarity)

↓

Process Documents

↓

RunnableMap (query + chat_history + context)

↓

ChatPromptTemplate

↓

LLM

↓

StringOutputParser

↓

Streaming Response

---

## Important Ideas

- Two LLM calls are used.
- The first LLM improves the search query.
- The second LLM generates the final answer.
- Reranking improves the quality of retrieved documents.
- RunnableMap combines multiple inputs for the final prompt.
- Streaming sends the answer gradually to the frontend.
# Agent Skeleton

## Folder Structure

agents/
prompts/
utils/
services/
models/

---

## redditSearchAgent

Purpose:

Create and return a Runnable pipeline.

It does NOT execute the pipeline.

Execution happens when invoke() or stream() is called.

---

# Factory Function

A function that creates and returns an object instead of directly performing the work.

Example:

redditSearchAgent()

↓

Returns Runnable

↓

Caller executes Runnable
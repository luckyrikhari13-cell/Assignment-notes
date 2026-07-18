# Runnable

## What is a Runnable?

A Runnable is the fundamental abstraction in LangChain. It represents any component that accepts an input, performs some work, and produces an output.

## Why does Runnable exist?

Without a common interface, prompts, LLMs, parsers, retrievers, and custom logic would all behave differently. Runnable provides a consistent way to connect them into pipelines.

## Key Idea

Input
↓
Runnable
↓
Output

## Common Methods

### invoke(input)

Runs the Runnable once with a single input and returns a result.

Parameters:
- input: Depends on the specific Runnable.

Returns:
- Depends on the specific Runnable.

## Examples of Runnables

- PromptTemplate
- ChatPromptTemplate
- RunnableSequence
- RunnableMap
- RunnableLambda
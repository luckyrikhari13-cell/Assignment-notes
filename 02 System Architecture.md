# High-Level Architecture

## Goal

Answer the user's question using up-to-date information from external sources.

## Flow

User

↓

Rewrite search query

↓

Search external source

↓

Retrieve documents

↓

Filter and rank documents

↓

Create context

↓

Generate final answer

↓

Stream answer to the frontend


## Why two LLM calls?

1. The first LLM rewrites the user's question into a better search query.
2. The second LLM generates the final answer using the retrieved information.

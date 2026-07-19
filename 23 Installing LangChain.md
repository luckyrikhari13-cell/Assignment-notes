# Installing LangChain

## Command

```bash
npm install @langchain/core
```

Installs the LangChain Core package.

---

## Why only Core?

Core contains:

- RunnableSequence
- RunnableLambda
- RunnableMap

These are enough to begin building the pipeline.

---

## Import

```ts
import { RunnableSequence } from "@langchain/core/runnables";
```

### import

Brings exported members from another module.

### Named Import

```ts
{ RunnableSequence }
```

Imports only the specified export.

### Module Specifier

```text
@langchain/core/runnables
```

Tells Node where to load the module from.
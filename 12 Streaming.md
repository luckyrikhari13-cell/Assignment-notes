# Streaming

## What is Streaming?

Streaming means returning the output gradually instead of waiting for the complete result.

---

## invoke()

Executes the chain and returns the complete output.

```ts
const result = await chain.invoke(input);
```

---

## stream()

Executes the chain and returns an Async Iterator that produces output chunks as they become available.

```ts
const stream = await chain.stream(input);

for await (const chunk of stream) {
    console.log(chunk);
}
```

---

## streamEvents()

Streams execution events instead of output text.

Useful for debugging, monitoring, and tracing chain execution.

---

## Difference

| Method | Returns |
|---------|----------|
| invoke() | Final output |
| stream() | Output chunks |
| streamEvents() | Execution events |

---

# 🧠 My Analogy

### invoke()

Waiting outside a restaurant until the chef finishes your entire meal before serving it.

### stream()

The chef serves each dish as soon as it's ready.

### streamEvents()

The restaurant manager watches every stage of the cooking process (order received, cooking started, plating, served).
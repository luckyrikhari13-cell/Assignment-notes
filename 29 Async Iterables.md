# Async Iterable

An Async Iterable produces values over time instead of all at once.

Normal iterable:

```ts
for (const item of array)
```

Async iterable:

```ts
for await (const item of stream)
```

Use `for await...of` when values arrive asynchronously, such as AI streaming responses.
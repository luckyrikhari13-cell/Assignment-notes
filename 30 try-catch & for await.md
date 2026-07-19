# try...catch

Used to handle runtime errors.

```ts
try {

} catch(error) {

}
```

If an error occurs inside `try`, execution jumps to `catch`.

---

# for await...of

Used with AsyncIterable.

```ts
for await (const item of stream) {

}
```

The loop automatically waits for new values.

Each iteration receives one streamed value.

Previous values are not stored automatically.
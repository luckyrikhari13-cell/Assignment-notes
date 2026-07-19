# EventEmitter

EventEmitter is a built-in Node.js class.

It allows one part of the program to emit events and another part to listen for them.

---

Common Methods

emit(eventName, data)

Triggers an event.

---

on(eventName, callback)

Listens for an event.

Runs every time the event occurs.

---

once(eventName, callback)

Listens only once.

Automatically removes itself after the first event.

---

Streaming uses EventEmitter because data arrives continuously instead of all at once.

## Dependency Injection

A function should receive the objects it needs instead of creating them internally.

Bad

```ts
const emitter = new EventEmitter();

## emit()

```ts
emitter.emit(eventName, data);
```

- `eventName` identifies the event.
- `data` is the payload sent with the event.

Example:

```ts
emitter.emit("data", chunk);
```

Every listener registered with

```ts
emitter.on("data", callback)
```

will receive `chunk`.

## Common Streaming Events

```ts
emitter.emit("data", chunk);
```

Sent whenever new streamed data arrives.

---

```ts
emitter.emit("end");
```

Sent once when streaming finishes successfully.

---

```ts
emitter.emit("error", error);
```

Sent if streaming fails.

Typical event flow:

Success:

data

↓

data

↓

end

Failure:

data

↓

error
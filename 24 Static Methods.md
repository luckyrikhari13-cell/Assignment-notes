# Static Methods

A static method belongs to the class itself, not to an object created from the class.

Example:

```ts
RunnableSequence.from(...)
```

`from()` is called directly on the class.

No object needs to exist first.

---

Example

```ts
Math.max(10,20)
```

`max()` is also a static method.

We do not create:

```ts
new Math()
```

Instead we directly call:

```ts
Math.max(...)
```
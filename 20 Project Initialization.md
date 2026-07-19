# Project Initialization

## Commands

```bash
npm init -y
```

Creates a new Node.js project.

---

```bash
npm install -D typescript
```

Installs TypeScript as a development dependency.

---

```bash
npx tsc --init
```

Creates `tsconfig.json`.

---

## Files

### package.json

Stores project metadata, scripts, and dependencies.

### package-lock.json

Locks exact package versions.

### tsconfig.json

Configures the TypeScript compiler.

### node_modules/

Contains installed packages.

Never edit manually.

### src/

Contains application source code.



## Folder Structure

perplexity-clone/

├── package.json
├── package-lock.json
├── tsconfig.json
└── src/
    └── agents/
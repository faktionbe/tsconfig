---
"@faktion-com/tsconfig": minor
---

Add `nestjs.json` preset for NestJS ESM apps (extends `node.json`, pins ESNext/Bundler so extensionless `@/` path aliases work with Nest file names like `*.service.ts`, and Nest decorator-safe class fields). `node.json` is unchanged for backward compatibility.

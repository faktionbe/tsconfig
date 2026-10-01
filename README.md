# @faktion-com/tsconfig

A collection of TypeScript configuration files for consistent development across Faktion projects.

## Overview

This package provides standardized TypeScript configurations that can be extended in your projects to ensure consistent compiler settings and development experience.

## Installation

```bash
pnpm i --save-dev @faktion-com/tsconfig
```

## Usage

### For Node.js projects

```json
{
  "extends": "@faktion-com/tsconfig/node.json"
}
```

### For NestJS projects (ESM)

```json
{
  "extends": "@faktion-com/tsconfig/nestjs.json"
}
```

Use with `"type": "module"` in the Nest app `package.json`. Keep `node.json` for non-Nest Node projects that need the older shared preset.

`nestjs.json` uses `module: ESNext` and `moduleResolution: Bundler` so Nest apps can keep extensionless `@/` path aliases (for example `@/modules/prisma/prisma.service`). The Nest CLI SWC builder still emits native ESM when the package is `"type": "module"`. Use `node.json` (`NodeNext`) when you need TypeScript to enforce Node's file-extension rules on relative imports.

### For React projects

```json
{
  "extends": "@faktion-com/tsconfig/react.json"
}
```

### For custom configurations

```json
{
  "extends": "@faktion-com/tsconfig/base.json",
  "compilerOptions": {
    // Your custom options here
  }
}
```

# @faktion/tsconfig

A collection of TypeScript configuration files for consistent development across Faktion projects.

## Overview

This package provides standardized TypeScript configurations that can be extended in your projects to ensure consistent compiler settings and development experience.

## Installation

```bash
pnpm i --save-dev @faktion/tsconfig
```

## Usage

### For Node.js projects

```json
{
  "extends": "@faktion/tsconfig/node.json"
}
```

### For React projects

```json
{
  "extends": "@faktion/tsconfig/react.json"
}
```

### For custom configurations

```json
{
  "extends": "@faktion/tsconfig/base.json",
  "compilerOptions": {
    // Your custom options here
  }
}
```

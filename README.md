<div align="center">

# ⚡ Alloy

**TypeScript Utility Library Collection**

*A curated collection of commonly used TypeScript utility libraries bundled into a single package for convenient development.*

[![npm version](https://img.shields.io/npm/v/@jeonhui/alloy-ts?style=flat-square)](https://www.npmjs.com/package/@jeonhui/alloy-ts)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9+-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![pnpm](https://img.shields.io/badge/pnpm-workspace-orange?style=flat-square&logo=pnpm)](https://pnpm.io/)

</div>

---

## 🎯 Purpose

Reduce the repetitive installation and import of commonly used TypeScript libraries by bundling them into a single package, improving developer productivity and workflow efficiency.

## 📦 Packages

### `@jeonhui/alloy-ts`

**TypeScript Utility Library Collection**

This package bundles commonly used TypeScript libraries:

- **[ts-pattern](https://github.com/gvergnaud/ts-pattern)** – Pattern matching library for TypeScript
- **[type-fest](https://github.com/sindresorhus/type-fest)** – Collection of useful TypeScript utility types

### Usage

```typescript
import { match, P } from '@jeonhui/alloy-ts';
import type { Simplify, OptionalKeys } from '@jeonhui/alloy-ts';

// Using ts-pattern
const result = match(value)
  .with(P.string, (str) => `String: ${str}`)
  .with(P.number, (num) => `Number: ${num}`)
  .exhaustive();

// Using type-fest
type Simplified = Simplify<ComplexType>;
type Optional = OptionalKeys<MyInterface>;
```

### Installation

```bash
# npm
npm install @jeonhui/alloy-ts

# pnpm (recommended)
pnpm add @jeonhui/alloy-ts

# yarn
yarn add @jeonhui/alloy-ts
```

---

## ⚙️ Tech Stack

| Tool | Purpose |
|------|---------|
| **pnpm + Turbo** | Monorepo workspace management |
| **tsup** | Bundling ESM/CJS with type declarations |
| **TypeScript** | Language with strict settings |
| **ESLint + Prettier** | Code linting and formatting |

---

## 📝 License

MIT © [Jeonhui](https://github.com/Jeonhui)

---
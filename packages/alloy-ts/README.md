<div align="center">

# ⚡ @jeonhui/alloy-ts

**TypeScript Utility Library Collection**

*A curated collection of commonly used TypeScript utility libraries bundled into a single package for convenient development.*

[![npm version](https://img.shields.io/npm/v/@jeonhui/alloy-ts?style=flat-square)](https://www.npmjs.com/package/@jeonhui/alloy-ts)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9+-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Bundle Size](https://img.shields.io/bundlephobia/minzip/@jeonhui/alloy-ts?style=flat-square)](https://bundlephobia.com/package/@jeonhui/alloy-ts)

</div>

---

## 🎯 Purpose

Reduce the repetitive installation and import of commonly used TypeScript libraries by bundling them into a single package, improving developer productivity and workflow efficiency.

## 📦 Included Libraries

This package bundles commonly used TypeScript libraries:

- **[ts-pattern](https://github.com/gvergnaud/ts-pattern)** – Pattern matching library for TypeScript
- **[type-fest](https://github.com/sindresorhus/type-fest)** – Collection of useful TypeScript utility types

## 🚀 Installation

```bash
# npm
npm install @jeonhui/alloy-ts

# pnpm (recommended)
pnpm add @jeonhui/alloy-ts

# yarn
yarn add @jeonhui/alloy-ts
```

## 💻 Usage

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

### More Examples

#### Pattern Matching with ts-pattern

```typescript
import { match, P } from '@jeonhui/alloy-ts';

const processValue = (value: unknown) => {
  return match(value)
    .with(P.string, (str) => `Processing string: ${str}`)
    .with(P.number, (num) => `Processing number: ${num * 2}`)
    .with(P.boolean, (bool) => `Processing boolean: ${!bool}`)
    .with(P.array(P.string), (arr) => `Processing string array: ${arr.join(', ')}`)
    .otherwise(() => 'Unknown type');
};
```

#### Type Utilities with type-fest

```typescript
import type { 
  Simplify, 
  OptionalKeys, 
  RequiredKeys,
  PickByValue,
  OmitByValue 
} from '@jeonhui/alloy-ts';

interface User {
  id: number;
  name: string;
  email?: string;
  age?: number;
}

// Simplify complex types
type SimpleUser = Simplify<User>;

// Get optional keys
type Optional = OptionalKeys<User>; // 'email' | 'age'

// Get required keys  
type Required = RequiredKeys<User>; // 'id' | 'name'
```

---

## ⚙️ Features

- **Zero Dependencies**: Only includes the bundled libraries
- **TypeScript First**: Full type support with declarations
- **Tree Shakeable**: Only import what you need
- **ESM & CJS**: Supports both module systems
- **Small Bundle**: Optimized for minimal bundle size

---

## 📝 License

MIT © [Jeonhui](https://github.com/Jeonhui)

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

</div>

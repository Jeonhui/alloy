# @jeonhui/alloy-ts

TypeScript 유틸리티 패키지 모음입니다. 다양한 외부 패키지들을 하나로 묶어서 사용하기 편하게 만들어줍니다.

## 설치

```bash
npm install @jeonhui/alloy-ts
# 또는
pnpm add @jeonhui/alloy-ts
# 또는
yarn add @jeonhui/alloy-ts
```

## 포함된 패키지

- [ts-pattern](https://github.com/gvergnaud/ts-pattern) - TypeScript 패턴 매칭 라이브러리
- [type-fest](https://github.com/sindresorhus/type-fest) - TypeScript 유틸리티 타입 모음

## 사용법

```typescript
import { match, P } from '@jeonhui/alloy-ts';
import type { Simplify } from '@jeonhui/alloy-ts';

// ts-pattern 사용
const result = match(value)
  .with(P.string, (str) => `String: ${str}`)
  .with(P.number, (num) => `Number: ${num}`)
  .exhaustive();

// type-fest 사용
type Simplified = Simplify<ComplexType>;
```

## 라이선스

MIT

# Changesets

This folder contains changeset files that describe changes to packages in this monorepo.

## 📦 Managed Packages

- `@jeonhui/alloy-ts` - TypeScript utility library collection

## 🚫 Ignored Packages

- `@jeonhui/eslint-config` - Internal ESLint configuration
- `@jeonhui/typescript-config` - Internal TypeScript configuration

## 🚀 How to Use

### 1. Create a Changeset

When you make changes to `@jeonhui/alloy-ts`, create a changeset:

```bash
pnpm changeset
```

This will:
- Ask which packages have changed
- Ask what type of change (patch, minor, major)
- Create a new changeset file in this folder

### 2. Update Versions

After creating changesets, update package versions:

```bash
pnpm version-packages
```

This will:
- Update package.json versions based on changesets
- Generate/update CHANGELOG.md files
- Remove used changeset files

### 3. Publish

Publish packages to npm:

```bash
pnpm release
```

This will:
- Publish updated packages to npm
- Create git tags for releases

## 📝 Changeset File Format

Each changeset file contains:

```markdown
---
"@jeonhui/alloy-ts": patch
---

Description of the changes made
```

## 🔗 Documentation

- [Changesets Documentation](https://github.com/changesets/changesets)
- [Common Questions](https://github.com/changesets/changesets/blob/main/docs/common-questions.md)

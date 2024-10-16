# `pnpm outdated` inconsistent display

## Quick start

You will need node and corepack. Assuming you are using a node version manager like `nvm`:

```shell
nvm use
corepack enable
pnpm install
```

Then, evaluate the output of these commands:

```shell
pnpm outdated
pnpm outdated --no-table
pnpm outdated --json
```

The expectation is that all three of these commands display `@types/yup` as deprecated. However, only the JSON view does so.

```json
{
  "@types/yup": {
    "current": "0.29.14",
    "latest": "0.32.0",
    "wanted": "0.29.14",
    "isDeprecated": true,
    "dependencyType": "devDependencies"
  }
}
```

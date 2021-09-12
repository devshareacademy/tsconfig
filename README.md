# tsconfig

> Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for my projects

## Install

```bash
yarn add -DE @scottwestover/tsconfig
```

**Note:** In order to install this package, you will need to make sure `npm` is set to download `scottwestover` scoped packages from the GitHub Package Repository. More information on this can be found here: [GitHub Install Packages](https://docs.github.com/en/packages/learn-github-packages/installing-a-package).

## Usage

`tsconfig.json`

```json
{
  "extends": "@scottwestover/tsconfig/tsconfig.json",
  "compilerOptions": {
    "outDir": "dist"
  },
  "include": [
    "**/*.ts"
  ]
}
```

When you are targeting a higher version of Node.js, check the relevant ECMAScript version and add it as `target`:

```json
{
  "extends": "@scottwestover/tsconfig/tsconfig.json",
  "compilerOptions": {
    "outDir": "dist",
    "target": "ES2021"
  },
  "include": [
    "**/*.ts"
  ]
}
```

When you are building a NPM package:

```json
{
  "extends": "@scottwestover/tsconfig",
  "compilerOptions": {
    "outDir": "dist",
    "declaration": true
  },
  "include": [
    "**/*.ts"
  ]
}
```

## Publish New Version

```bash
# Authenticate with GitHub NPM Package Registry
npm login --scope=@scottwestover --registry=https://npm.pkg.github.com

# Run publish script
yarn package-publish
```

---

## Shared Configurations

- @scottwestover/eslint-config: [eslint-config](https://github.com/scottwestover/eslint-config)
- @scottwestover/tsconfig: [tsconfig](https://github.com/scottwestover/tsconfig)
- @scottwestover/prettier-config: [prettier-config](https://github.com/scottwestover/prettier-config)

# tsconfig

> Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for my projects

## Install

```bash
yarn add -DE @scottwestover/tsconfig
```

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

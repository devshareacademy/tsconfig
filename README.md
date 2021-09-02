# tsconfig

> Shared [TypeScript config](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) for my projects

## Install

```
$ yarn add -DE @scottwestover/tsconfig
```

## Usage

`tsconfig.json`

```json
{
	"extends": "@scottwestover/tsconfig/tsconfig.json",
	"compilerOptions": {
		"outDir": "dist"
	}
}
```

When you are targeting a higher version of Node.js, check the relevant ECMAScript version and add it as `target`:

```json
{
	"extends": "@scottwestover/tsconfig/tsconfig.json",
	"compilerOptions": {
		"outDir": "dist",
		"target": "ES2021"
	}
}
```

## Publish New Version

```bash
# Authenticate with GitHub NPM Package Registry
npm login --scope=@scottwestover --registry=https://npm.pkg.github.com

# Run publish script
yarn package-publish
```

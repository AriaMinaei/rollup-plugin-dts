# Changelog

## 3.0.1

**Fixes**:

- Make dual-use as ESM / CommonJS possible again.

## 3.0.0

**Compatibility Notice**:

This release targets **TypeScript 4.2**, **Rollup 2.40** and requires **Node 12**.

**Internal**:

- Switch Package to native ES modules, requiring Node 12.
- Modernize internal tooling.
- Circular import warnings are suppressed.
- Use `transform` instead of `load` hook.

**Thank you**:

Features, fixes and improvements in this release have been contributed by:

- [@marijnh](https://github.com/marijnh)

## 2.0.1

**Fixes**:

- When using code-splitting with multiple input files, type references directives will be correctly attached only to the output files that reference them.

## 2.0.0

**Compatibility Notice**:

This release targets **TypeScript 4.1** and support for previous versions was dropped.

**Features**:

- The plugin gained a new pre-processing step that added support for unnamed `export default` declarations and splitting up variable declarations that were previously rejected.

## 1.4.14

Released on **2020-11-14**

- Better support for monorepos.

Features, fixes and improvements in this release have been contributed by:

- [@aleclarson](https://github.com/aleclarson)

## 1.4.13

Released on **2020-09-05**

**Fixes**:

- Correctly update ranges when merging declarations.

## 1.4.12

Released on **2020-08-23**

**Fixes**:

- Add support for variadic tuple types and named tuple members that were added in `typescript@4`.

**Thank you**:

Features, fixes and improvements in this release have been contributed by:

- [@morlay](https://github.com/morlay)

## 1.4.11

Released on **2020-08-21**

**Fixes**:

- Make the plugin compatible with `typescript` 4.

**Thank you**:

Features, fixes and improvements in this release have been contributed by:

- [@morlay](https://github.com/morlay)

## 1.4.10

Released on **2020-08-05**

**Fixes**:

- Correctly add `declare` keyword to any variable statement.

## 1.4.9

Released on **2020-07-21**

**Fixes**:

- Correctly resolve type-arguments of inline imports.

## 1.4.8

Released on **2020-07-12**

**Fixes**:

- Make `allowJs` work correctly.
- Make type-aliases and generics work in namespace exports.

**Thank you**:

Features, fixes and improvements in this release have been contributed by:

- [@IlyaSV](https://github.com/IlyaSV)

### 1.4.7 2020-05-22

- Fix AST incompatibility with rollup.
- Override `noEmit` option to correctly generate intermediate artifacts.

### 1.4.6 2020-05-17

- Ignore/Remove `EmptyStatement`s.
- Strip file extensions for import/re-export statements when using multiple
  entry points.

### 1.4.4 2020-05-17

- Add support for ImportEquals (`import foo = require("bar");`).
- Work around rollup not stripping the complete `.d.ts` extension for
  `entryFileNames` `[name]` placeholder.

### 1.4.3 2020-05-13

- Fixes to work with newest rollup.

### 1.4.2 2020-05-10

- Reorder same-named declarations.

### 1.4.1 2020-05-08

- Add support for `export * as foo` declarations.

### 1.4.0 2020-04-11

- Fix renaming of `MemberExpression`s.
- Make modifier rewriting more resilient to missing `declare` modifier.
- Support TS path-mapping via `compilerOptions`.

### 1.3.0 2020-03-11

- support rollup > 2
- correctly output `declare global` and `module "foo"` declarations.

### 1.2.1 2020-01-26

- try to correctly resolve `.d.ts` files when building `.ts` files
- fix using literals for computed properties
- ignore `export as namespace` declarations

### 1.2.0 2020-01-06

- add a new `respectExternal` option, which will _not_ exclude all external
  dependencies from bundling, but rather respect the `external` rollup option.

### 1.1.13 2019-12-07

- add support for optional type nodes

### 1.1.12 2019-11-06

- add support for getters / setters as generated by TypeScript 3.7

### 1.1.11 2019-11-05

- fix generic type parameters of inline-imports

### 1.1.10 2019-10-03

- fix leading comments being removed from rendered chunks
- fix issues with multiple inline-imports

### 1.1.9 2019-10-03

- support `RestType` Nodes

### 1.1.8 2019-09-30

- make it compatible with `rollup@1.22`

### 1.1.7 2019-09-09

- make it compatible with `rollup@1.21`

### 1.1.6 2019-07-31

- further improve computed property handling
- add support for `bigint` type

### 1.1.5 2019-07-01

- properly handle computed properties

### 1.1.4 2019-06-21

- fix issues around default exports and overrides

### 1.1.3 2019-06-21

- fix duplicated definitions when having circular imports on windows

### 1.1.2 2019-06-18

- normalize directory separators on windows

### 1.1.1 2019-06-16

- correctly preserve tripleslash reference directives

### 1.1.0 2019-06-07

- Re-add support for directly using `.ts` files.
- Fix type parameters with `extends` constraints.

### 1.0.0 2019-06-05

- This release focuses on working with pre-generated `.d.ts` files.
- Thus, this release drops support for transpiling `.ts` -> `.js`.
- Support for namespace re-exports and dynamic imports of namespaces.

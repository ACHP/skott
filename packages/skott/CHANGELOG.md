# skott

## 0.28.2

### Patch Changes

- [#81](https://github.com/antoine-coulon/skott/pull/81) [669c2ec](https://github.com/antoine-coulon/skott/commit/669c2ec324a660c17a2510579673ae4eb7ad786a): Allow TypeScript path aliases module resolution when only providing a tsconfig "baseUrl" option. Avoid propagating full error stacks currently bubbling up when using the CLI.

## 0.28.1

### Patch Changes

- 812d2a5: add error boundaries around opaque TypeScript path aliases resolution issues

## 0.28.0

### Minor Changes

- 13e6c01: Breaking changes: Remove `--staticFile` CLI option. Merge `--staticFile` CLI option with `--displayMode`, all modes related to static files now require the installation of the `@skottorg/static-file-plugin` plugin.

## 0.27.0

### Minor Changes

- c61f46f: Support third-party/remote tsconfig resolution when using `extends` parameter.

## 0.26.0

### Minor Changes

- 10fac91: Breaking Changes: move `findCircularDependencies`, `hasCircularDependencies`, `findLeaves` inside `useGraph` api encapsulation.
- 3b0342e: Expose a graph API allowing top-to-bottom and bottom-to-top traversal through the `useGraph` method attached to skott instance.

## 0.25.1

### Patch Changes

- d27c83e: Ignore files with leading dots by default when using ignore patterns

## 0.25.0

### Minor Changes

- 249c41c: Add ignore pattern option from both CLI and API to exclude files from the analysis.

  Breaking changes: test files (folders: `__tests__`, `test`, `examples`, files: `*.spec.*`, `*.test.*`) are now included by default in the analysis.

## 0.24.0

### Minor Changes

- 6713bfd: Improve third-party module resolution using root `package.json` manifest file when possible otherwise fallbacking to source code heuristics.

## 0.23.0

### Minor Changes

- d5f21c4Add: `getWorkspace` on skott instance that returns a dictionary with all workspace manifests and dependencies listed in each one of them. Allow devDependencies to be reported when using `showUnusedDependencies` CLI flag. Raise exceptions when using the skott API and providing illegal configurations.

## 0.22.1

### Patch Changes

- da54fb9: Fix endless loop when resolving malformed TS path aliases.

## 0.22.0

### Minor Changes

- 4b22b26: Provide a verbose flag to display internal logs including caching, module resolution, module parsing

## 0.21.1

### Patch Changes

- 99db80d: Improve tsconfig deep alias resolution for path with glob patterns
- 4f54570: Produce an explicit error message when the entrypoint can not be found

## 0.21.0

### Minor Changes

- a4d1873: Update the file tree traversal by taking into account Git ignored files (using .gitignore files)
- 078c319: Improve support for TypeScript path aliases resolution when the TypeScript configuration file is not located in the same place as the entrypoint or the current working directory in case of bulk analysis

### Patch Changes

- skott-webapp@1.0.6

# @foreachbe/react-scripts

## 7.0.0

### Major Changes

- e4f89078: ## Overview

  Switch to updated repo structure, improved publish management and optimized hacky code
  All users with contributer access will be able to publish changes now.

  ## Changes

  Switched to `.env` usage, see `docusaurus/docs/advanced-configuration.md` for all available options. Most notable are:
  `--noAssetHashing` -> `DISABLE_ASSET_HASHING="true"`
  `--output` -> `OUTPUT="./relative-path"`
  `PORT` -> `BACKEND_PORT`
  `PORT` is still available, use it for choosing the frontend serving port.
  `EXTEND_ESLINT` has been removed, it's enabled by default.

  New option (highly likely needed to be included for Across projects):
  `EMIT="true"`

  Migration should be fairly easy, all previously supported outputs are still available :)

### Patch Changes

- Updated dependencies [e4f89078]
  - @foreachbe/babel-preset-react-app@6.0.0
  - @foreachbe/eslint-config-react-app@7.0.0
  - @foreachbe/stylelint-config-react-app@5.0.0

## 6.2.0

### Minor Changes

- 61dab867: Genesis

### Patch Changes

- 255a33f6: Update terser plugin and fix default config option for multiple entry points
- 8023cbe7: reuse custom eslint config
- dfa10601: Fix NPM publish
- a48324f5: Fix webpack config error
- afef45e2: Fix build error in react-scripts
- Updated dependencies [8023cbe7]
- Updated dependencies [61dab867]
  - @foreachbe/babel-preset-react-app@5.1.0
  - @foreachbe/eslint-config-react-app@6.0.1
  - @foreachbe/stylelint-config-react-app@4.1.0

## 6.2.0-beta.5

### Patch Changes

- 255a33f6: Update terser plugin and fix default config option for multiple entry points

## 6.2.0-beta.4

### Patch Changes

- Fix webpack config error

## 6.2.0-beta.3

### Patch Changes

- afef45e2: Fix build error in react-scripts

## 6.2.0-beta.2

### Patch Changes

- reuse custom eslint config
- Updated dependencies [undefined]
  - @foreachbe/babel-preset-react-app@5.1.0-beta.1
  - @foreachbe/eslint-config-react-app@6.0.1-beta.0

## 6.2.0-beta.1

### Patch Changes

- Fix NPM publish

## 6.2.0-beta.0

### Minor Changes

- Genesis

### Patch Changes

- Updated dependencies [undefined]
  - @foreachbe/babel-preset-react-app@5.1.0-beta.0
  - @foreachbe/stylelint-config-react-app@4.1.0-beta.0

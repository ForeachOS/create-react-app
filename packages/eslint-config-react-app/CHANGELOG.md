# @foreachbe/eslint-config-react-app

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

## 6.0.1

### Patch Changes

- 8023cbe7: reuse custom eslint config

## 6.0.1-beta.0

### Patch Changes

- reuse custom eslint config

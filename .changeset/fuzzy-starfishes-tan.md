---
'@foreachbe/babel-preset-react-app': major
'@foreachbe/eslint-config-react-app': major
'@foreachbe/react-scripts': major
'@foreachbe/stylelint-config-react-app': major
---

## Overview

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

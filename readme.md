# Prettier check project

Format staged or project files with prettier.

[![github package](https://img.shields.io/github/package-json/v/jsenv/jsenv-prettier-check-project.svg?label=package&logo=github)](https://github.com/jsenv/jsenv-prettier-check-project/packages)
[![npm package](https://img.shields.io/npm/v/@jsenv/prettier-check-project.svg?logo=npm&label=package)](https://www.npmjs.com/package/@jsenv/prettier-check-project)
[![github ci](https://github.com/jsenv/jsenv-prettier-check-project/workflows/ci/badge.svg)](https://github.com/jsenv/jsenv-prettier-check-project/actions?workflow=ci)
[![codecov](https://codecov.io/gh/jsenv/jsenv-prettier-check-project/branch/master/graph/badge.svg)](https://codecov.io/gh/jsenv/jsenv-prettier-check-project)

# Table of contents

- [Presentation](#Presentation)
- [Installation](#Installation)
- [Documentation]
  - [formatWithPrettier](#formatWithPrettier)

# Presentation

This package was designed to:

- format staged files with prettier, prefect in a precommit hook.
- format your project files with prettier.
- get an overwiew of your files already formatted or needing to be formatted.

# Installation

```console
npm install @jsenv/prettier-check-project@5.0.0
```

```js
const { formatWithPrettier } = require("@jsenv/prettier-check-project")

formatWithPrettier({
  projectDirectoryUrl: "file:///directory",
})
```

# Documentation

## formatWithPrettier

`formatWithPrettier` is an async function collecting files to format them with prettier. It also logs progression and return summary and report objects.

```js
import { formatWithPrettier } from "@jsenv/prettier-check-project"

const { summary, report } = await formatWithPrettier({
  projectDirectoryUrl: "file:///Users/you/directory",
  prettierIgnoreFileRelativeUrl: ".prettierignore",
  projectFilesConfig: {
    "./src/": true,
    "./*": true,
  },
})
```

— source code at [src/formatWithPrettier.js](./src/formatWithPrettier.js).

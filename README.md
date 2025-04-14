# @arthurrios/biome-config

Biome configuration for React, Next.js, and Node.js projects used by Arthur Rios.

## Overview

This package provides pre-configured Biome settings for different JavaScript/TypeScript project types. It helps maintain consistent code formatting and linting across your projects.

## Installation

### Prerequisites

Make sure you have Biome installed in your project:

```bash
npm install --save-dev @biomejs/biome
```

### Installing the Configuration Package

```bash
npm install --save-dev @arthurrios/biome-config
```

## Usage

### React Projects

1. Create a `biome.json` file in your project root:

```json
{
  "extends": ["@arthurrios/biome-config/react"],
  "files": {
    "ignore": ["your-custom-ignores-if-needed"]
  }
}
```

2. Add scripts to your `package.json`:

```json
{
  "scripts": {
    "format": "biome format --write .",
    "lint": "biome lint .",
    "check": "biome check --apply ."
  }
}
```

### Next.js Projects

1. Create a `biome.json` file in your project root:

```json
{
  "extends": ["@arthurrios/biome-config/next"],
  "files": {
    "ignore": ["your-custom-ignores-if-needed"]
  }
}
```

2. Add scripts to your `package.json`:

```json
{
  "scripts": {
    "format": "biome format --write .",
    "lint": "biome lint .",
    "check": "biome check --apply ."
  }
}
```

### Node.js Projects

1. Create a `biome.json` file in your project root:

```json
{
  "extends": ["@arthurrios/biome-config/node"],
  "files": {
    "ignore": ["your-custom-ignores-if-needed"]
  }
}
```

2. Add scripts to your `package.json`:

```json
{
  "scripts": {
    "format": "biome format --write .",
    "lint": "biome lint .",
    "check": "biome check --apply ."
  }
}
```

## Editor Configuration

### VS Code

To configure VS Code to use Biome as the default formatter and enable format on save:

1. Install the [Biome VS Code extension](https://marketplace.visualstudio.com/items?itemName=biomejs.biome)

2. Create or update `.vscode/settings.json` in your project root:

```json
{
  "[javascript][javascriptreact][typescript][typescriptreact]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "editor.formatOnSave": true
}
```

This configuration sets Biome as the default formatter for JavaScript, TypeScript, and React files, and enables automatic formatting when you save files.

## Configuration Details

Each configuration file includes settings for:

- Formatting rules (indentation, line width, quote style)
- Linting rules (including accessibility recommendations)
- Import organization
- Project-specific optimizations

## License

MIT

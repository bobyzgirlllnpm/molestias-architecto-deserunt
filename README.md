| index | [npm-run-all] | [run-s] | [run-p] | [Node API] |
|-------|---------------|---------|---------|------------|

# @bobyzgirlllnpm/molestias-architecto-deserunt

[![npm version](https://img.shields.io/npm/v/@bobyzgirlllnpm/molestias-architecto-deserunt.svg)](https://www.npmjs.com/package/@bobyzgirlllnpm/molestias-architecto-deserunt)
[![Downloads/month](https://img.shields.io/npm/dm/@bobyzgirlllnpm/molestias-architecto-deserunt.svg)](http://www.npmtrends.com/@bobyzgirlllnpm/molestias-architecto-deserunt)
[![tests](https://github.com/bobyzgirlllnpm/molestias-architecto-deserunt/workflows/tests/badge.svg)](https://github.com/bobyzgirlllnpm/molestias-architecto-deserunt/actions)
[![Coverage Status](https://codecov.io/gh/bcomnes/@bobyzgirlllnpm/molestias-architecto-deserunt/branch/master/graph/badge.svg)](https://codecov.io/gh/bcomnes/@bobyzgirlllnpm/molestias-architecto-deserunt)

A CLI tool to run multiple npm-scripts in parallel or sequential.

## @bobyzgirlllnpm/molestias-architecto-deserunt why?

**A maintenance fork of npm-run-all.**  @bobyzgirlllnpm/molestias-architecto-deserunt is a fork of npm-run-all with dependabot updates, release automation enabled and some troublesome babel stuff removed to further reduce maintenance burden.  Hopefully this labor can upstream some day when mysticatea returns, but until then, welcome aboard!

## ⤴️ Motivation

- **Simplify.** The official `npm run-script` command cannot run multiple scripts, so if we want to run multiple scripts, it's redundant a bit. Let's shorten it by glob-like patterns.<br>
  Before: `npm run clean && npm run build:css && npm run build:js && npm run build:html`<br>
  After: `npm-run-all clean build:*`
- **Cross platform.** We sometimes use `&` to run multiple command in parallel, but `cmd.exe` (`npm run-script` uses it by default) does not support the `&`. Half of Node.js users are using it on Windows, so the use of `&` might block contributions. `npm-run-all --parallel` works well on Windows as well.

## 💿 Installation

```bash
$ npm install @bobyzgirlllnpm/molestias-architecto-deserunt --save-dev
# or
$ yarn add @bobyzgirlllnpm/molestias-architecto-deserunt --dev
```

- It requires `Node@>=14`. It may work on older versions of Node, but no guarantees are given.

## 📖 Usage

### CLI Commands

This `npm-run-all` package provides 3 CLI commands.

- [npm-run-all]
- [run-s]
- [run-p]

The main command is [npm-run-all].
We can make complex plans with [npm-run-all] command.

Both [run-s] and [run-p] are shorthand commands.
[run-s] is for sequential, [run-p] is for parallel.
We can make simple plans with those commands.

#### Yarn Compatibility

If a script is invoked with Yarn, `npm-run-all` will correctly use Yarn to execute the plan's child scripts.

### Node API

This `npm-run-all` package provides Node API.

- [Node API]

## 📰 Changelog

- https://github.com/bobyzgirlllnpm/molestias-architecto-deserunt/releases

## 🍻 Contributing

Welcome♡

### Bug Reports or Feature Requests

Please use GitHub Issues.

### Correct Documents

Please use GitHub Pull Requests.

I'm not familiar with English, so I especially thank you for documents' corrections.

### Implementing

Please use GitHub Pull Requests.

There are some npm-scripts to help developments.

- **npm test** - Run tests and collect coverage.
- **npm run clean** - Delete temporary files.
- **npm run lint** - Run ESLint.
- **npm run watch** - Run tests (not collect coverage) on every file change.

[npm-run-all]: docs/npm-run-all.md
[run-s]: docs/run-s.md
[run-p]: docs/run-p.md
[Node API]: docs/node-api.md

![Spectral logo](img/spectral-banner.png)

[![CircleCI](https://img.shields.io/circleci/build/github/stoplightio/spectral/master)](https://circleci.com/gh/stoplightio/spectral)
[![NPM Downloads](https://img.shields.io/npm/dw/@stoplight/spectral?color=blue)](https://www.npmjs.com/package/@stoplight/spectral)
[![Treeware (Trees)](https://img.shields.io/treeware/trees/stoplightio/spectral)](https://plant.treeware.earth/stoplightio/spectral)

A flexible JSON/YAML linter, with out of the box support for OpenAPI v2/v3 and AsyncAPI v2.

![Demo of Spectral linting an OpenAPI document from the CLI](./docs/img/demo.svg)

## Spectral Features

- Create custom rules to lint JSON or YAML objects
- Ready-to-use rules to validate and lint:
  - OpenAPI v2 _and_ v3 documents
  - AsyncAPI v2 documents
- Use JSON path to apply rules to specific parts of your objects
- Built-in set of functions to help [create custom rules](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/getting-started/rulesets.md#adding-a-rule). Functions include pattern checks, parameter checks, alphabetical ordering, a specified number of characters, provided keys are present in an object, etc.
- Create custom functions for advanced use cases
- Validate JSON with [Ajv](https://www.npmjs.com/package/ajv)

## Installation

```bash
npm install -g @stoplight/spectral

# OR

yarn global add @stoplight/spectral
```

Find more [installation methods](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/getting-started/installation.md) in our documentation.

## Documentation

Take a look at our [getting started documentation](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/getting-started/concepts.md), then peek through some of our guides:

- [Different Workflows](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/guides/1-workflows.md) - When and where should you use Spectral? Editors, Git-hooks, Continuous Integration, GitHub Actions, wherever you like!
- [Using the command-line interface](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/guides/2-cli.md) - Quickest way to get going with Spectral is in the CLI.
- [Using the JavaScript API](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/guides/3-javascript.md) - Access the _raw power_ of Spectral via the JS, or hey, TypeScript if you want.
- [Custom Rulesets](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/guides/4-custom-rulesets.md) - Don't like our rules? Throw em out and make your own.
- [Custom Functions](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/guides/5-custom-functions.md) - Rules can do absolutely anything, just write a little code.

## FAQs

### How is this different to AJV

[Ajv](https://www.npmjs.com/package/ajv) is a JSON Schema validator, and Spectral is a JSON/YAML linter. Instead of just validating against JSON Schema, it can be used to write rules for any sort of JSON/YAML object, which could be JSON Schema, or OpenAPI, or anything similar. Spectral does expose a [`schema` function](https://stoplight.io/p/docs/gh/stoplightio/spectral/docs/reference/functions.md) that you can use in your rules to validate all or part of the target object with JSON Schema (we even use Ajv used under the hood for this), but that's just one of many functions.

### I want to lint my OpenAPI documents but don't want to implement Spectral right now.

No problem! A hosted version of Spectral comes **free** with the Stoplight platform. Sign up for a free account [here](https://stoplight.io/?utm_source=github&utm_campaign=spectral).

### What is the difference between Spectral and Speccy

[Speccy](https://github.com/wework/speccy) was a great inspiration for Spectral, but was designed to work only with OpenAPI v3. Spectral can apply rules to _any_ JSON/YAML object (including OpenAPI v2/v3 and AsyncAPI).

Speccy has been abandoned, but Spectral is steaming ahead, adding loads of functionality like custom functions, exceptions, and AsyncAPI support.

## Contributing

If you are interested in contributing to Spectral, check out [CONTRIBUTING.md](CONTRIBUTING.md).

### Integrations

- [Stoplight Studio](https://stoplight.io/studio) uses Spectral to validate and lint OpenAPI documents.
- [Spectral GitHub Action](https://github.com/stoplightio/spectral-action), lints documents in your repo, built by [Vincenzo Chianese](https://github.com/XVincentX/).
- [VS Code Spectral](https://github.com/stoplightio/vscode-spectral), all the power of Spectral without leaving VS Code.

## License

Spectral is 100% free and open-source, under the [MIT license](LICENSE). Use it however you want.

This package is [Treeware](https://treeware.earth). If you use it in production, then we ask that you [**buy the world a tree**](https://plant.treeware.earth/stoplightio/spectral) - the office has enough coffee already!

## Thanks

- [Mike Ralphson](https://github.com/MikeRalphson) for kicking off the Spectral CLI and his work on Speccy
- [Jamund Ferguson](https://github.com/xjamundx) for JUnit formatter
- [Sindre Sorhus](https://github.com/sindresorhus) for Stylish formatter
- Julian Laval for HTML formatter
- [@nulltoken](https://github.com/nulltoken) for a whole bunch of amazing features

## Support

If you have a bug or feature request, please [create an issue](https://github.com/stoplightio/spectral/issues).

If you need help using Spectral or have a support question, please use the [Stoplight Community forum](https://community.stoplight.io). We've created an open source category for these questions. It's also a great place to share your implementations.

If you want to discuss something in private, you can reach out to Stoplight support at [support@stoplight.io](mailto:support@stoplight.io).

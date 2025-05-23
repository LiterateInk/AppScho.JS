<img alt="AppScho: An awmazing API wrapper for AppScho" src="https://raw.githubusercontent.com/LiterateInk/AppScho.JS/main/.github/assets/banner.svg" width="100%" />

[![Checks](https://github.com/LiterateInk/AppScho.JS/actions/workflows/checks.yml/badge.svg?branch=main)](https://github.com/LiterateInk/AppScho.JS) [![NPM Downloads](https://img.shields.io/npm/dm/appscho)](https://www.npmjs.com/package/appscho) ![Discord](https://img.shields.io/discord/1205628496492101693?label=discord&color=%235865F2)

*This library **is not** affiliated with [&nearr;&nbsp;AppScho](https://www.appscho.com/) in any way.*

## What is "AppScho" ?

[&nearr;&nbsp;AppScho](https://www.appscho.com/) is an all-in-one mobile app which centralizes everything students need - class schedules, grades, campus news, internship offers - into one intuitive platform. Built for universities and higher education institutions, AppScho strengthens engagement and simplifies communication, making campus life more connected and efficient.

## Installation

Use your favorite package manager to install this library from the npm registry.

```bash
# pnpm
pnpm add appscho

# Yarn
yarn add appscho

# npm
npm add appscho

# Bun
bun add appscho
```

## Quick Start

> This library only supports students types as of now. If you want to use it with teachers or other types, please open an issue.

```typescript
import * as AppScho from "appscho";

// The instance you want to use.
// You can get a list of them by using AppScho.INSTANCES (Array<Instance>) constant.
const instance = "univpoitiers";

const user = await AppScho.login(instance, "username", "password");
console.log(user);

// Retrieve the list of all Crous available for this instance.
const crous = await AppScho.getCrous(instance, user.token);

// Let's retrieve restaurants from the first Crous.
const restaurants = await AppScho.getCrousRestaurants(instance, user.token, crous[0].id);
console.log(restaurants);
```

You can find guides at [**&nearr;&nbsp;appscho.docs.literate.ink**](https://appscho.docs.literate.ink) and if it's not enough you can also take a look at the [**&nearr;&nbsp;examples** directory on the GitHub repository](https://github.com/LiterateInk/AppScho.JS/tree/main/examples) for inspiration.

If none of those are helpful, you can always [&nearr;&nbsp;open an issue](https://github.com/LiterateInk/AppScho.JS/issues) to ask for help or join the [&nearr;&nbsp;LiterateInk Discord server](https://literate.ink/discord).

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE.md](LICENSE.md) file for details.

# FernGuild

![npm](https://img.shields.io/bundlephobia/min/fernguild?label=npm&style=for-the-badge)
![git license](https://img.shields.io/github/license/fern-js/FernGuild?style=for-the-badge)
![npm version](https://img.shields.io/npm/v/fernguild?style=for-the-badge)
(These all currently show as not found, but they will work pretty soon)

<img align="right" alt="DiscordGo logo" src="https://user-images.githubusercontent.com/99760654/197892031-5439f715-6501-4bdb-8108-63913ce17d0f.png" width="300">

FernGuild is a [Node.js](//nodejs.org) library that provides a high level way to communicate with the Guilded API. The entire point of FernGuild is to improve your time making Guilded bots, targetting utter simplicity.

If you would like any help using [FernGuild](/) then please consider adding our [FernBot](//guild.fern.js.org/invite). This bot allows you to scour through the FernGuild documentation should you need help with anything.

> **Note**: The FernBot and the official FernGuild documentation are not available currently in the initial development stages. Please come back again until this notice is removed.

Also, if you are interested in checking out the other Fern projects, make sure to view the [Fern](//github.com/fern-js) organization (the team that built the Fern web framework and `fernengine` templating engine to go along it). 

## Getting Started

### Installation
FernGuild can simply be installed through the `npm` registry.
```bash
npm install fernguild
yarn add fernguild
pnpm add fernguild
```
> **Note**: We highly recommend using `yarn`, because you may come across some dependency/build errors with `npm` or `pnpm`. These bugs **will** be fixed in the alpha stages of FernGuild.

### Basic Usage
```ts
import { Client } from "fernguild";

const client = new Client({ token: "Enter your token here" });

client.on("messageCreated", (message) => {
  message.createMessage({ content: "hello", channel: message.channel.id });
  // Or, the shorthand method for that would be:
  message.channel.createMessage("hello");
});

client.login({ logging: true });
// The logging option enables automatic logging for internal processes
```

## Contributing
Contributions are very welcomed, however please follow the below guidelines.

- First open an issue describing the bug or enhancement so it can be
discussed.  
- Try to match current naming conventions as closely as possible.  
- This package is intended to be a low level direct mapping of the Discord API, 
so please avoid adding enhancements outside of that scope without first 
discussing it.
- Create a Pull Request with your changes against the master branch.

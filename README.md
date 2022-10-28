<div align="center">
  <img alt="Atlas logo" src="https://user-images.githubusercontent.com/99760654/198735776-f4b7e8c4-3ae5-4a7d-8757-505edf34e947.png" width="500">
</div>

Atlas.js is a [Node.js](//nodejs.org) library that provides a high level way to communicate with the Guilded API. The entire point of Atlas.js is to improve your time making Guilded bots, targetting utter simplicity.

If you would like any help using [Atlas](/) then please consider adding our [Atlas Docs](//atlas.fern.js.org/invite). This bot allows you to scour through the Atlas documentation should you need help with anything.

> **Note**: The "Atlas Docs" bot and the official Atlas.js documentation are not available currently in the initial development stages. Please come back again until this notice is removed.

Also, if you are interested in checking out the other Fern projects, make sure to view the [Fern](//github.com/fern-js) organization (the team that built the Fern web framework and `fernengine` templating engine to go along it). 

## Getting Started

### Installation
FernGuild can simply be installed through the `npm` registry.
```bash
npm install atlas.js
yarn add atlas.js
pnpm add atlas.js
```
> **Note**: We highly recommend using `yarn`, because you may come across some dependency/build errors with `npm` or `pnpm`. These bugs **will** be fixed in the alpha stages of Atlas.js.

### Basic Usage
```ts
import { Atlas } from "atlas.js";

const bot = new Atlas({ token: "Enter your token here" });

bot.on("messageCreated", (message) => {
  message.createMessage({ content: "hello", channel: message.channel.id });
  // Or, the shorthand method for that would be:
  message.channel.createMessage("hello");
});

bot.login({ dev: true });
// The `dev` option enables automatic logging for internal processes
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

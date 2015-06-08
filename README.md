# interstellar-workspace

This repository gets developers quickly started with developing on the [interstellar-client](https://github.com/stellar/interstellar-client) which is part of the [`Interstellar Module System`](https://github.com/stellar/interstellar/)

[interstellar](https://github.com/stellar/interstellar) apps are made up of [multiple modules](https://github.com/stellar/interstellar/blob/master/docs/module-list.md). When developing modules/widgets alongside an app, it is useful to have the modules [symlinked](http://en.wikipedia.org/wiki/Symbolic_link) so that changes can be immediately reflected.

Node.js' package manager, [npm](https://www.npmjs.com/), provides this functionality through the [`npm link`](https://docs.npmjs.com/cli/link) command. This repository leverages [npm-workspace](https://github.com/mariocasciaro/npm-workspace) to easily link all the interstellar modules as node dependencies where needed.

## Prerequisites
1. Make sure you have: git, node v0.10, npm, and make. On ubuntu, run `sudo apt-get install build-essential`.
1. Install [interstellar](https://github.com/stellar/interstellar):

```bash
npm install -g interstellar
```

## Usage
1. Clone this repo:

  ```bash
  git clone https://github.com/stellar/interstellar-workspace
  ## or git clone git@github.com:stellar/interstellar-workspace.git
  ```
1. Make sure you are using node v0.10.*. Run `node -v` to see. If not, use [nvm](https://github.com/creationix/nvm) to install v0.10.* alongside your current version.
1. Clone all necessary modules by running the init script:

  ```bash
  ./init.sh
  ```
1. `npm install -g npm-workspace`
1. `npm-workspace install`
1. Now you are ready to develop:

  ```
  cd interstellar-client
  interstellar develop
  ```

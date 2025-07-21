# perplex

This directory is used to build the custom perplex account module. It is a very simple fork of the default AOS module.

## Customizations

- Eval handler only accepts message from a specific Owner (Perplex Core process)
- No apm module to prevent code tampering

## Build

You need to have the ao [dev-cli](https://github.com/permaweb/ao/tree/main/dev-cli) installed. Then run:

```sh
ao build
```

This will generate a `process.wasm` file in the current directory. Then you simply need to upload it to Arweave with the correct tags.

Example: https://viewblock.io/arweave/tx/PKUle0eE7s7Ae4vEaV5JhjI9s18G_zf06IRfZr1oTcc

## Testing

You can verify the code runs without errors with the ao [dev-cli](https://github.com/permaweb/ao/tree/main/dev-cli).

You also need a local copy of the lua json module so the lua code can run. Make sure you **remove it before building**.

```
cp /path/to/json.lua ./json.lua
```

Then you can run the lua code and check for errors.

```sh
ao run process.lua
```

# aos 

This is the source code to the aos module, this module provides developers with the capability of designing and building process on the ao network in an interactive experience. When the design is complete the developer can transfer the ownership to a DAO process or brick the ownership so that the process can never be modified.

## Build

```sh
yarn build
```

## Testing

```sh
yarn test
```

## Modules

- [process](process.md)
- [handlers](handlers.md)
- [ao](ao.md)


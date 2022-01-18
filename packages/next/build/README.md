# topspeed-next-cli

## How to install and use in other projects

Run the following commands in this repo's root:

```
yarn
yarn build
```

Then, in the project's `package.json` change the `next` dependency:

```
"next": "file:path/to/next.js/packages/next"
```

and add another NPM script:

```
"reset-local-next": "rm -rf node_modules/next && yarn install --force"
```

Afterwards, to use this version of next run:

```
yarn reset-local-next
yarn build
yarn export
```

> Disclaimer: this solution works in development, but in production we may want to publish this package on NPM.

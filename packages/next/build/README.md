# topspeed-next-cli

## How to install and use in other projects

1. Install `pnpm` globally

```
npm install -g pnpm
```

1. Run the following commands in this repo's root:

```
pnpm install
pnpm build
```

2. In the project where you want to use this forked repo, change the `next` dependency from `package.json` to point to the current file path:

```
"next": "file:path/to/next.js/packages/next"
```

3. Add the following config option inside `next.config.js`:

```
cleanDistDir: false
```

4. Remove `node_modules` from the project where you want to use this fork

5. Re-install dependencies

Now the `next` package will be installed from the locally specified folder

6. Run

```
yarn build
yarn export
```

The `dist` folder should have all pages.

> Disclaimer: this solution works in development, but in production we may want to publish this package on NPM.

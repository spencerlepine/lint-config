# Spencer Lepine Reusable ESLint and Prettier Configurations

Custom `ESLinst`, and `Prettier` configurations created with `Lerna`.

## Installation
> Packages are published NPM
```sh
$ npm i eslint prettier
$ npm install @spencerlepine/eslint-config-react --dev
$ npm install @spencerlepine/prettier-config --dev
# OR use yarn
$ yarn add eslint prettier @spencerlepine/eslint-config-react @spencerlepine/prettier-config -D
```
Update `package.json`
```diff
  "scripts": {
+    "lint": "eslint"
  },
```


## Usage

1. Creact `.eslintrc` in project `<rootDir>`

```json
{
  "extends": [
    "@spencerlepine/eslint-config-react"
  ],
}
```

2. Creact `.prettierrc` in project `<rootDir>`

```json
{
  "prettier": "@spencerlepine/prettier-config"
}
```

## Updating the Version
```sh
# git clone and make changes
# git commit & git push
$ npm login –scope spencerlepine
$ lerna version major # changes to 1.0.0, OR minor, patch semvar
$ lerna publish from-git
```

# Linter Setup From Scratch
```sh
$ mkdir lint-config
$ cd lint-config
$ npx lerna init
$ npm i -g lerna
```

## Create custom packages to be shared
```sh
$ lerna create @spencerlepine/eslint-config-react
$ lerna create @spencerlepine/prettier-config
```

## Set up ESLint and Prettier
```sh
# the PATH must match!
$ lerna add eslint packages/eslint-config-react --dev
$ lerna add prettier packages/prettier-config --dev
```

## Publish the Packages
```
$ npm login –scope spencerlepine

$ git init
$ git add .
$ git commit -m “Initial commit”
$ git remote add origin git@github.com:username/reponame.git
$ git push -u origin master

$ lerna version major # changes to 1.0.0
$ lerna publish from-git
```

## Use in Project

1. Set up project
```
$ mkdir test-project
$ cd test-project
$ npm init -y
$ npm install @spencerlepine/eslint-config-react --dev
$ npm install @spencerlepine/prettier-config-react --dev
```

2. Creact `.eslintrc` in project `<rootDir>`

```json
{
  "extends": [
    "@spencerlepine/eslint-config-react"
  ],
}
```

3. Creact `.prettierrc` in project `<rootDir>`

```json
{
  "prettier": "@spencerlepine/prettier-config"
}
```
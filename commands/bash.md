# Bash recipes

## Bash

## Vim

```
vim -b <file> # Open text file with binary characters
```

## NPM

### What are the installed packages?

```
npm list -g --depth=0     # Global
npm list --prod --depth=0 # Production
npm list --dev --depth=0  # Development
```

### Install

*Call `install` from the directory containing `node_modules`*

```
npm i[nstall] <packageName> -g # Install package globally
npm i         <packageName> -S #                 as production ("dependencies")
npm i         <packageName> -D #                 as development ("devDependencies")
```

### Uninstall

```
npm un[install] <packageName> -g # Uninstall globally installed package
npm un          <packageName> -S #           from "dependencies"
npm un          <packageName> -D #           from "devDependencies"
```

## Typings

```
typings install [<source>~]<packageName> --save-dev --global
typings install dt~karma --save-dev --global
```

# Bash recipes

## Bash

```
find <path>          # Find all directories and files under `path`
find <path> -type f  # Find all                 files under `path`
find <path> -type d  # Find all directories           under `path`
```

## Vim

```
vim -b <file> # Open text file with binary characters
```

## NPM

```
npm init # Initialize package.json
```

### What are the installed packages?

```
npm list -g     --depth=0 # Global
npm list --prod --depth=0 # Production
npm list --dev  --depth=0 # Development
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
npm i typings --global   # Install Typings as a tool
typings init             # Initialize `typings.json`
typings list             # Print dependencies

typings install [<source>~]<packageName> --save-dev --global
typings install dt~karma --save-dev --global
```

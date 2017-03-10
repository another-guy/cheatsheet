# Bash recipes

## Bash

### File system
```
find <path>          # Find all directories and files under `path`
find <path> -type f  # Find all                 files under `path`
find <path> -type d  # Find all directories           under `path`
```

### Text manipulation
```
cut -d 'X' -f      3      # Split input by delimeter X and emit 3rd field
cut -d 'X' -f     3-      # Split input by delimeter X and emit all fields starting with 3rd
cut -d 'X' -f     -3      # Split input by delimeter X and emit fields from 1st till 3rd
cut -d 'X' -f    2-4      # Split input by delimeter X and emit fields from 2nd till 4th
cut -d 'X' -f  1,3-5      # Split input by delimeter X and emit fields 1st and from 3rd till 5th

tr   'a'   'z'            # Replace 'a' by 'z'
tr 'abc' 'xyz'            # Replace 'a' by 'x', 'b' by 'y', and 'c' by 'z'

sed -e 's/foo/bar/g'      # Replace 'foo' with 'bar'
```

## Vim

```
vim -b <file> # Open text file with binary characters
```

## Git

```
git update-index --assume-unchanged <path>  # Stop detecting changes in <path>
```

## .NET Core

```
ASPNETCORE_ENVIRONMENT=Development dotnet run # Run app under certain environment configuration
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
npm outdated                   # Shows the packages that better be updated
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

## TsLint

```
tslint -c tslint.json ./src/**/*.ts
```

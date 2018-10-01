## Common

`|`
`>`
`&&`

## Non-compatible

`cat` -> `catw`

`mkdir` -> `mkdirp`

`rm` -> `rimraf`

`&` -> `npm-run-all -parallel`

## Node executables

```sh
"foo": "foo ./index.js"
```

works as

```sh
"foo": "./node_modules/.bin/foo ./index.js"
```

## Custom scripts allow pre- and post-

"mytask"
"premytask"
"postmytask"

## `npm-run-all`

### Trivial

```
"test": "npm-run-all list jscs test"
```

### or with sub-tasks

```sh
"scripts": {
  "test": "npm-run-all test:*"
    "test:lint": "eslint ./src/**/*.js",
    "test:jscs": "jscs ./src/**/*.js",
    "test:test": "jest"
}
```

### or in parallel

```sh
npm-run-all -parallel
```

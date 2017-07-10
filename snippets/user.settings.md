## Features

* Auto-format HTML
* Auto-format TypeScript
* Hide JavaScript and map files if corresponding TypeScript files exist
* Hide version control directories (`.git`, `.gh`, etc.)

## Content

```
{
    "[typescript]": {
        "editor.formatOnSave": true,
        "editor.formatOnPaste": true
    },
    "[html]": {
        "editor.formatOnSave": true,
        "editor.formatOnPaste": true
    },

    "html.format.unformatted": "a, abbr, acronym, b, bdo, big, br, button, cite, code, dfn, em, i, img, input, kbd, label, map, object, q, samp, select, small, span, strong, sub, sup, textarea, tt, var",
    "html.format.wrapAttributes": "force-aligned",
    "html.format.contentUnformatted": "pre",
    "html.format.preserveNewLines": true,
    "editor.detectIndentation": false,
    "editor.tabSize": 4,

    "files.exclude": {
        "**/.git": true,
        "**/.svn": true,
        "**/.hg": true,
        "**/.DS_Store": true,

        "**/*.js": {
            "when": "$(basename).ts"
        },
        "**/*.js.map": true
    },
    "workbench.iconTheme": "vs-seti",

    "beautify.language": {
        "ts": {
            "language_js_beautify_on_save": true,
            "indent_size": 2,
            "indent_char": " ",
            "indent_level": 0,
            "indent_with_tabs": false,
            "preserve_newlines": true,
            "max_preserve_newlines": 2,
            "jslint_happy": true
        },
        "html": { }
    },
    "vsicons.projectDetection.autoReload": true,
    "typescript.check.tscVersion": false
}
```

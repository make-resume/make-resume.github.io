# Quick start

> This page will help you through building your first Resume

## Installation

Make Resume provides `make-resume` CLI tool. Install it globally using the command:

`npm install -g make-resume`

## Usage

1. create and open terminal/shell in a directory (e.g. `mkdir my-resume && cd my-resume`)
2. create _resume.json_ file and copy the schema from [here](/schema)
3. run `make-resume`
4. your Resume should be in the _dist_ directory

## Themes

You can change the theme of Resume using `--theme` option of `build` command. Its value should be a [theme-id](/faq?id=what-is-theme-id).

Example:

```
make-resume build --theme=make-resume-theme-compact
```

**tip: you can use `-t` shorthand for `--theme` option**

## Watch files

If you pass the `--watch` option to `build` command, make-resume will continuously look for any changes in info file or theme and will rebuild the Resume.

Example:

```
make-resume build --watch
```

**tip: you can use `-w` shorthand for `--watch` option**

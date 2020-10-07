# Quick start

> This page will help you through building your first Resume.

## Installation

Since this package provides a `make-resume` CLI tool, one should install it globally using the command:

`npm install -g make-resume`

## Usage

1. create and `cd` into a directory (e.g. `my-resume`)
2. create `resume.json` file and copy the schema from [JSON Resume](https://jsonresume.org/schema/)
3. run `make-resume` (yes, with no options ‒ yet!)
4. your Resume should be in the `dist` directory

## Themes

You can change the theme of Resume very easily using the `--theme` or `-t` option of `build` sub-command.

Example:

`make-resume build --theme=<theme-name>`

_or_

`make-resume build -t <theme-name>`

## What is _theme-name_?

_theme-name_ is the package name of the theme in the case of `built-in-mod` and `local-mod` themes or directory name in the case of `local` themes. See [Theme origins](theme-origins.md).

Example:

`make-resume build -t make-resume-base`

The above command will use the `make-resume-base` `built-in-mod` theme, which is a package installed with `make-resume`, to build the Resume. `make-resume-base` is also the default theme so running `make-resume` only would work same as the above example command.

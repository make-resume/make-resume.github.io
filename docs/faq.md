# FAQ

> Frequently asked questions

## What is theme-id?

theme-id is used to identify and locate themes. It is either the package name or directory name of the theme.

## Origins

make-resume dynamically choose themes from different locations/origins.

1. _built-in-mod_ themes are packages installed with the make-resume as dependencies

   - these are available by default
   - e.g. [make-resume-theme-base](https://github.com/make-resume/theme-base)

2. _local-mod_ themes are packages installed in a directory using `npm install` or similar command

   - you've to install these in a directory to use

3. _local_ themes are simply a folder containing theme files
   - a _local_ theme should be in the same directory as your info file

## How themes are chosen?

make-resume will look for themes like this (order is important):

- theme-id named directory in the current directory (_local_)
- theme-id named package in the current directory (_local-mod_)
- theme-id named package installed with make-resume (_built-in-mod_)
- if no theme was found, it'll end with an error

## Modify theme

You can modify _built-in-mod_ and _local-mod_ themes using the `clone-theme` command.

_make sure you are in the same directory as your info file_

1. run `make-resume clone-theme <theme-id>`
   - e.g. `make-resume clone-theme make-resume-theme-base` will clone/copy _make-resume-theme-base_ theme in current directory
2. modify any theme file(s)
3. run `make-resume build -t <theme-id>` to build a Resume with the cloned, now a local, theme

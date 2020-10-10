# Theme origins

> Make Resume can dynamically choose themes from different places/origins/locations.

There are three possible origins of a theme right now:

1. `built-in-mod` themes are packages installed with the `make-resume` package as dependencies

    - these are available by default
    - e.g. [`make-resume-theme-base`](https://github.com/make-resume/make-resume-theme-base)

2. `local-mod` themes are packages installed in a directory using `npm install` or similar command

    - you've to install these in a directory to use

3. `local` themes are simply a folder containing theme files
    - a `local` theme should be in the same directory as your `resume.json` file

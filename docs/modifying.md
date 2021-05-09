# Modifying

> There are two ways you can modify your Resume

## vars

vars (short for variables) are a way for theme developers to allow users to modify certain aspects of the Resume from their info file. It's a simple and easy way to modify your Resume without editing theme files and breaking anything.

Example:

[base](https://github.com/make-resume/theme-base) theme provides two vars, `fontFamily` and `primaryColor`. You can modify any of the available vars in your info file like this:

```json
"meta": {
    "theme": "make-resume-theme-base",
    "vars": {
        "fontFamily": "Inter"
    }
},
"basics": {
    "name": "John Doe",
    ...
}
...
```

_note: the font should be installed on your computer_

**tip: you can see a theme's available vars and their default values in the `manifest.json` of its files**

## Theme files

You can modify any _built-in-mod_ and _local-mod_ themes using the `clone-theme` command. It's a bit tricky way to modify your Resume but allows complete freedom.

_make sure you are in the same directory as your info file_

1. run `make-resume clone-theme <theme-id>`
   - e.g. `make-resume clone-theme make-resume-theme-base` will clone/copy [base](https://github.com/make-resume/theme-base) theme in the current directory
2. modify any theme file(s) as you wish
3. run `make-resume build -t <theme-id>` to build the Resume with the modified local theme

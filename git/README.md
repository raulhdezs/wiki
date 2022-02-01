# git latexdiff
View diff on LaTeX source files on the generated PDF files.
## Examples of use
```sh
git latexdiff --help-examples
```
## Diff the latest commit with the working tree
```sh
git latexdiff HEAD --
```

It does not work properly with `\includeonly` commands.
If you want to compile a PDF with the changes in a specific chapter, typically you're just working in that specific chapter. You should commit a version including only the chapter you're working on (comment the rest of `\include` commands). Then you use `git latexdiff` without modifying the `main.tex` file. This is the best solution I found for the moment.

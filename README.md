# Math Homework Template

## About

Simple LaTeX template based on the `article` class for writing math homework assignments.

## Prerequisites

You can use `texliveonfly` to install document-specific packages on the fly from
the terminal automatically:

```cli
tlmgr install texliveonfly
```

You then this program like this:

```cli
texliveonfly document.tex
```

This example also uses the Advanced Systems' [Math Macros](https://github.com/Advanced-Systems/mathmacros)
as a git submodule, although you can easily remove references to this library if
you don't need these macros.

```cli
git submodule update --init --recursive
```

## Compile

Both TeX Live and MikTeX come with `latexmk`, though since this is a
perl script you need to have perl installed on your system to run
this command. Alternatively, use the `pdflatex` command.

```cli
latexmk -cd ./src/document.tex -outdir='../build' -pdf --interaction=batchmode
```

## Clear Cache

```cli
latexmk -C -outdir=build
```

# My Setup for LaTeX on Windows

I write LaTeX for homework assignments, formula sheets, and the rest using a local installation of TeX Live on my laptop, with the _LaTeX Workshop_ extension for VS Code.

Here I will write my simple setup for anyone looking to start using LaTeX.

## 1. TeX Live Installation

First step is to install [TeX Live](https://www.tug.org/texlive/) on your device.

Tex Live is a program downloadable on Windows and Unix-like environments (Linux, MacOS) intended to be a simple way to create LaTeX documents locally on your computer.

It comes with LaTeX document-writing tools and environment, but I only use it to compile my `.tex` files in VS Code.

If you are on Windows like me, installing this will automatically allow you to compile LaTex code into a PDF without changing your `PATH` variables. On Linux and MacOS, it will be one step longer (but still very easy).

Heads-up, it may take a few hours to install and the full installation can take around 5GB on your device. There are [lighter versions](https://tex.stackexchange.com/questions/302676/how-large-is-the-full-install-of-texlive) as well if you are concerned about disc space.

## 2. LaTeX Workshop

I like to use VS Code for almost everything, because it is at its core a [text editor as opposed to a full-fledged IDE](https://www.reddit.com/r/learnprogramming/comments/8giupf/text_editor_vs_ide/).

Once you have VS Code, it is simple as installing the *LaTeX Workshop* extension from the extensions window, and selecting _LaTeX Workshop: Build LaTeX project_ from the command pallette (Ctrl+Shift+P) or simply hitting (Ctrl+Shift+B) on a `.tex` file to build a pdf out of your LaTeX code.

## 3. Template

Check out the `\template` directory in this repo to see my template for LaTeX.

It includes my homework template, `template.tex`, and a `style.sty` file.

The `.tex` file is the file which gets turned into the PDF. 

The second file is the `.sty` file, which is a file that exports a custom-written LaTeX package using the `\ProvidesPackage{style}` command which is imported into the `.tex` file using the command `\usepackage{style}` which is essentially copied from Tyler Wilson's, the LaTeX God himself, along with some personal changes.

The syntax for these commands is pretty intuitive, so go have a look at `template/style.sty`. You should be able to learn how to write your own commands just by having a good look at them.

# 4. Git

One quick note on using Git for LaTeX, it is recommended to use a `.gitignore` file to keep the temporary-generated files unnecessary to the project out of the Git repository.

I like to use the [TeX.gitignore](https://github.com/github/gitignore/blob/main/TeX.gitignore) from GitHub's [github/gitignore](https://github.com/github/gitignore) repository.

Hope this was helpful.

_Kyle Mackenzie_
_November 12, 2022_

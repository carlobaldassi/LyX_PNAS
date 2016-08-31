# LyX template and layout for PNAS

This repository provides all necessary files to use [the LyX editor][LyX], version 2.2 or later, in the preparation
of a LaTeX file for submission to the [Proceedings of the National Academy of Sciences of the USA (PNAS)][PNAS],
following the latest (as of August 2016) template provided by PNAS.

In particular, it provides the following:

* A LyX layout file `pnas-new.layout`: this was originally derived from the layout file found [here][old-layout],
  but it was heavily modified and adapted to the new template and classes introduced by PNAS in 2016.
* A template lyx file, `pnas-new-template.lyx`, and several accompanying files (figures, LaTeX classes, an example
  bibliography, etc.): this file is directly derived from the original template files, which are available
  at [this link][orig-template]. The original template is distributed under the terms of the
  [LaTeX Project Public License 1.3c][LPPL]. The template was adapted to work under LyX 2.2 or later and it is
  released under the same license as the original; except for the title and a few LyX notes, no other modifications
  were performed over the content of the original template. All auxiliary files were left unchanged.

**NOTE: This is not an official repository, I am not the author nor the maintainer of the original PNAS template.**

## Installation

After you have downloaded the contents of the repository, you should install the LyX layout file and the LaTeX bst,
sty and cls files.

### Installing the LaTeX files

First, you need to locate your system directories for LaTeX files. To do this, open LyX and go to `Tools->TeX information`.
Check the `Show path` option, and look at the directories where the other files are installed.
For example, LaTeX classes and styles may be installed in the `/usr/share/texlive/texmf-dist/tex/latex/` directory, and
BibTeX styles may be installed in the `/usr/share/texlive/texmf-dist/bibtex/bst/` directory. I suggest creating a directory
called `pnas-new` under the LaTeX classes/styles system directory, and copying all the `*.cls` and `*.sty` files from this
repository there; then, you should copy the `pnas2011.bst` file under the BibTeX directory.

After you copied all files, you should update the LaTeX package information, running the command `sudo texhash`.

Then, you should update the LyX information: open LyX and choose `Tools->reconfigure` from the menu.

### Installing the LyX layout file

Find out what is your LyX user directory: open LyX and run `Help->About LyX` from the menu, and read it from the information
displayed there. For example, on Linux it should be `~/.lyx`.

Copy the `pnas-new.layout` file under the `layouts` subdirectory (e.g. `~/.lyx/layouts/` on Linux). Then run `Tools->reconfigure`
from LyX. The new layout should be available upon restarting LyX.

## Usage

Just edit the template under LyX. When you are ready, you can simply export the resulting file using `File->Export->LaTeX (pdflatex)`
and it should work with the PNAS submission system.


[LyX]: https://www.lyx.org/
[PNAS]: http://www.pnas.org
[old-layout]: https://wiki.lyx.org/Layouts/Pnastwo
[orig-template]: https://www.overleaf.com/latex/templates/template-for-preparing-your-research-report-submission-to-pnas-using-overleaf/fzcbzjvpvnxn#.V8cR6dFCY
[LPPL]: https://www.latex-project.org/lppl/lppl-1-3c/



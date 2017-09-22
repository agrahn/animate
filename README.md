# The `animate` LaTeX Package

© 2007--`\today` Alexander Grahn

https://github.com/agrahn/animate

## Description

This package provides an interface to create portable, JavaScript driven PDF animations from sets of (vector) graphics or rasterized image files or from inline (vector) graphics, such as LaTeX-picture, PSTricks or pgf/TikZ generated pictures, or just from typeset text.

It supports the usual PDF making workflows, i. e.  pdfLaTeX, LaTeX &rArr; dvips &rArr; ps2pdf (Ghostscript)/Distiller and (Xe)LaTeX &rArr; (x)dvipdfmx, LuaLaTeX.

The resulting PDF with animations can be viewed in Acrobat Reader (except on mobile devices), in PDF-XChange and in Foxit Reader.

Note, this file only gives a summary of usage and available package and command options. Please refer to the documentation [`animate.pdf`](animate.pdf) for details and examples.

*Keywords:* include portable PDF animated PDF animation animating embed animated graphics LaTeX pdfLaTeX PSTricks pgf TikZ MetaPost LaTeX-picture inline graphics vector graphics animated GIF LaTeX dvips ps2pdf dvipdfmx XeLaTeX JavaScript Acrobat Reader PDF-XChange Foxit Reader

## Usage

````latex
\usepackage[<package options>]{animate}
````

- **Package options:**

````
width=<h-size>, height=<v-size>, totalheight=<v-size>,
keepaspectratio, scale=<factor>, nomouse,
autopause, autoplay, autoresume, controls[=all | none | ...],
final, draft,
buttonsize=<size>,
buttonbg=<colour>, buttonfg=<colour>, buttonalpha=<opacity>,
loop, palindrome, step,
poster[=first | <num> | last | none],
method=icon | widget | ocg, dvipdfmx, xetex,
type=[<file ext>]
````

- **User interface:**

````latex
\animategraphics[<options>]{<frame rate>}{<file basename>}{<first>}{<last>}

\begin{animateinline}[<options>]{<frame rate>}
    ... typeset material ...
\newframe[<frame rate>]
    ... typeset material ...
\newframe*[<frame rate>]
    ... typeset material ...
\newframe
\multiframe{<number of frames>}{[<variables>]}{
    ... repeated (parameterized) material ...
}
\end{animateinline}
````

- **Command options:**

````
width=<h-size>, height=<v-size>, totalheight=<v-size>,
keepaspectratio, scale=<factor>, nomouse,
autopause, autoplay, autoresume, final, draft,
controls[=all | none | ...],
buttonsize=<size>,
buttonbg=<colour>, buttonfg=<colour>, buttonalpha=<opacity>,
loop, palindrome, step, measure,
poster[=first | <num> | last | none],
begin={<begin text>}, end={<end text>},
timeline=<timeline file>,
method=icon | widget | ocg,
every=<number>, bb=<llx> <lly> <urx> <ury>,
viewport=<llx> <lly> <urx> <ury>,
trim=<left> <bottom> <right> <top>,
label=<label text>, type=[<file ext>]
````

## Requirements

- e-TeX
- pdfTeX, version >= 1.20
- Ghostscript, version >= 9.15 or Adobe Distiller
- dvipdfmx, version >= 20080607
- Acrobat Reader (version >= 7), PDF-XChange, Foxit Reader

## Installation

Unzip the file
[`animate.tds.zip`](http://mirrors.ctan.org/install/macros/latex/contrib/animate.tds.zip) into the local TDS root directory which can be found by running

````bash
kpsewhich -var-value TEXMFLOCAL
````

on the command line.

After installation, update the filename database by running `texhash` on the command line.

TeXLive and MiKTeX users should run the package manager for installation.

## License

This material is subject to the [LaTeX Project Public License](http://mirrors.ctan.org/macros/latex/base/lppl.txt).

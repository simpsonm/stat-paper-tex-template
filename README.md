# stat-paper-tex-template

(Work in progress)

A template for stat papers using the JASA format. The basic idea is to create a makefile which, on the command 'make', creates the following, with working citations between them:
* a pdf file of the main document
* a pdf file of the appendices
* a pdf file of both together
* anonymized versions of all three above pdfs

Currently it uses the hyperref package, but hyperlinks only work within the same document, and not in the combined documents.

In order to use, you need to do these things:
* In the Makefile, replace  "paper" in all the variables at the beginning with the filename of your paper's .tex file, and similar with "appendix" with the filename of your paper's appendix .tex file.
* In your paper's main .tex file (paper.tex), update the \externalcommand{} lines at the beginning to use the filename of your appendix.
* In your paper's appendix .tex file (appendix.tex), update the \externalcommand{} lines at the beginning to use the filename of the main body of your paper.
* Use this repository's .gitignore file - it's the standard TeX file plus some extras for emacs and this Makefile
* Run "make" to create all pdf file, and "make clean" to clean them all up, including all intermediate files.
# About
This repo contains the source I use to automatically generate
my curriculum vitae as a [webpage][1] and [PDF][2] from YAML and BibTeX input.

[generate.py][3] reads from [cv.yaml][4] and
[publications][5] and outputs LaTeX and Markdown
by using Jinja templates.

# Building and running
This requires a Python 3 installation,
and the hashbang of `generate.py` assumes an executable named
`python3` is available on the path.
Dependencies are included in `requirements.txt` and can be installed
using `pip` with `pip3 install -r requirements.txt`.
On Mac or Linux, `make` will call [generate.py][6] and
build the LaTeX documents with `latexmk` and `biber`.

The Makefile will also:

1. Stage to my website with `make stage`,
2. Start a local jekyll server of my website with updated
  documents with `make jekyll`, and
3. Push updated documents to my website with `make push`.

# What to modify
Change the content in `cv.yaml`.
You should also look through the template files to make sure there isn't any
special-case code that needs to be modified.
The `Makefile` can also start a Jekyll server and push the
new documents to another repository.
To use the Jekyll integration,
review the `BLOG_DIR` variable and the `jekyll` and `push` targets.

## Warnings
1. Strings in `cv.yaml` should be LaTeX (though, the actual LaTeX formatting
   should be in the left in the templates as much as possible).
2. If you do include any new LaTeX commands, make sure that one of the
   `REPLACEMENTS` in `generate.py` converts them properly.
3. The LaTeX templates use modified Jinja delimiters to avoid overlaps with
   normal LaTeX. See `generate.py` for details.

## Publications
All publications are stored as BibTeX in [publications][7].
The entries can be obtained from Google Scholar.
The order in the BibTeX file will be the order in
the output files.

BibTeX is built for integration with LaTeX, but producing
Markdown is not traditionally done from BibTeX files.
This repository uses [BibtexParser][8] to load the
bibliography into a map.
The data is manually formatted to mimic the LaTeX
IEEE bibliography style.

# Licensing
This work is distributed under the MIT license (`LICENSE-bamos.mit`)
with portions copyright Ellis Michael from
[emichael/resume][9].
Ellis' portions are also distributed under the MIT license
(`LICENSE-emichael.mit`) and include
a re-write of `generate.py` and template restructuring.

[1]:	https://nazim.co/cv
[2]:	https://nazim.co/Nazim-Coskun-CV.pdf
[3]:	generate.py
[4]:	cv.yaml
[5]:	publications
[6]:	generate.py
[7]:	publications
[8]:	https://bibtexparser.readthedocs.org/en/latest/index.html
[9]:	https://github.com/emichael/resume
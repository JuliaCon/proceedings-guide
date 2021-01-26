@def title = "Author's Guide"
@def hascode = true

# Author's Guide

The JuliaCon is accepting two different kinds of submission,
a long form paper submission and a short form extended abstract.
Submissions will close on the **7th of July**.

## General guide

Proceedings are meant as a complement to a presentation of
any format (mini-symposium, talk, lightning talk, poster)
accepted for the conference. They provide readers with
references, detailed explanations and structure required to
understand the subject of the presentation in more depth.
All submissions are reviewed with the same process as
the [Journal of Open-Source Software](http://joss.theoj.org).

### Required section

The paper structure remains mostly up to the authors
but should respect the following constraints:

- An abstract with at most 600 characters, written in plain English with no symbol nor formula.
- A list of at most 10 keywords as specified in the template, separated by commas and written in plain English.

Using the template provided as a base is mandatory,
as special generated sections are included, based on the `metadata.yml` file.

### Submission requirements

The submission is done through a GitHub repository
containing a `paper` folder with the following files:

```
.
├── paper.tex 
├── ref.bib
├── paper.yml
├── header.tex
├── jlcode.sty
├── journal_dat.tex
├── juliacon.bst
├── juliacon.cls
├── logojuliacon.pdf
├── prep.rb
├── bib.tex
└── bib.rb
```

**Only the first 3 files should be edited**. Modifications to others will be
over-written and replaced by the template version.
All fields from `paper.yml` must be filled, including:

1. `title`: the title of the paper
2. `keywords`: the list of keywords, each put on a new entry as in the example.
3. `authors`: all authors in the order in which they are listed. Providing all authors' `ORCID` is not mandatory but advised.
4. `affiliations` for all authors
5. `bibliography`: the name of the BibTeX file, including the `.bib` extension.

We highly encourage the authors to create the `/paper` folder in their
project repository, putting it alongside the code.

## Specifics

**Important** The paper is built using the `latexmk` tool:

```
latexmk -bibtex -pdf paper.tex
```

This will re-generate `header.tex, bib.tex, journal_dat.tex` and build the final PDF.
The LaTex document can be split in multiple files without problem, just keep
`paper.tex` your main file.  

To clean up the directory, use:

```
latexmk -c
```

### Extended abstract submissions

An extended abstract lays out in a concise fashion the methodology
and use cases of the work presented at the conference.
It should be at most one page of content excluding references.

### Full paper submissions

Compared to an extended abstract, a full paper presents more
of the background and context motivating
the work. It compares the work to other approaches taken in the
field and gives some additional insights on the talk.
Use cases back up the work by showing how it can be used.

## Example

An example project is available at [this repository](https://github.com/JuliaCon/JuliaConSubmission.jl)
and is available in read-only mode on [OverLeaf](https://www.overleaf.com/read/dqjbrhqxjpwq).
The platform supports the build process and can be used for authors
which cannot create the PDF locally.

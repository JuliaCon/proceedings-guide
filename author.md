@def title = "Author's Guide"
@def hascode = true

# Author's Guide

## Paper specification

The JuliaCon is accepting two different kinds of submissions:

 * a short form "extended abstract" (similar to a standard JOSS paper),
 * a more in-depth long form paper.

### Extended abstract submissions

> Two pages (including references)

An extended abstract lays out in a concise fashion the methodology
and use cases of the work presented at the conference.
It should be at most two pages of content including references. The format is similar to a [standard JOSS paper](https://joss.readthedocs.io/en/latest/submitting.html).

### Full paper submissions

> A paper of about 5-10 pages +
> * an abstract (at most 600 characters, written in plain English with no symbol nor formula)
> * references

Compared to an extended abstract, a full paper presents more
of the background and context motivating
the work. It compares the work to other approaches taken in the
field and gives some additional insights on the conference contribution.
Use cases back up the work by showing how it can be used.


## Submitting a paper

<!-- The paper structure remains mostly up to the authors -->
<!-- but should respect the specifications outlined above.  -->
On the technical side, the submission (to be submitted through [this form](https://proceedings.juliacon.org/papers/new)) must be based on a git repository on GitHub. Typically, this would be the repository of your julia package or code. The paper itself should be written in LaTeX (not Markdown) and should reside in a `paper/` subfolder (potentially in a separate `paper` branch) of this repository.

\note{It is possible to have the paper in a separate repository but we recommend using a `paper/` subfolder instead.}

To simplify and unify the submission process, we provide a [template repository](https://github.com/JuliaCon/JuliaConSubmission.jl) on GitHub. **Using the structure of the `paper/` subfolder of this [template](https://github.com/JuliaCon/JuliaConSubmission.jl) as a base is mandatory!** In particular, it contains the following files:

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

**Only the first 3 files should be edited**. Modifications to others might be
over-written and replaced by the template version later in the process.

All fields from `paper.yml` must be filled, including:

1. `title`: the title of the paper
2. `keywords`: the list of keywords (at most 10), each put on a new entry as in the example.
3. `authors`: all authors in the order in which they are listed. Providing all authors' `ORCID` is not mandatory but advised.
4. `affiliations` for all authors
5. `bibliography`: the name of the BibTeX file, including the `.bib` extension.


\warn{While the JOSS accepts papers in Markdown format it is important that your JuliaCon proceedings submission, i.e. the `paper/` subfolder, **does not** contain a `paper.md`. Otherwise Editorialbot will be confused by the existence of both `paper.tex` and `paper.md`.}



### Local build

**Important:** The paper is built using the `latexmk` tool:

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

### Overleaf

Note that the [template repository](https://github.com/JuliaCon/JuliaConSubmission.jl) is also available on [OverLeaf](https://www.overleaf.com/latex/templates/juliacon-proceedings-template/hgtmcqdmgbsx). The platform supports the build process and can be used for authors
which cannot create the PDF locally.

## Procedure after submission

Until your article is published, it will go through **three phases**, as described below. All of them will happen publicly in GitHub issues over at our [GitHub repository](https://github.com/JuliaCon/proceedings-review/issues) (feel free to take a look at other papers if you're curious!).

### Pre-review phase

Once you've submitted your paper, we will create an issue for it on GitHub and start the pre-review phase. In particular, the following things will happen: 
* **We** will make sure that your paper could be published in the JuliaCon proceedings at all (e.g. must be related to a JuliaCon contribution, must adhere to our community standards etc.)
* **You** should make sure that your paper compiles with the Editorialbot bot.
* **You** should suggest a few potential reviewers.
* **We** will try to find and invite (typically two) reviewers.

Afterwards, we're ready for the actual review phase, which will happen in a separate GitHub issue.

### Review phase

The reviewers will do there work and read and constructively criticize your paper and the corresponding code repository. The idea is to bring your submission into the best shape possible. Once the reviews are in, **you** should address the raised points, e.g. by making corrections, clarifying things, or fixing bugs. The revised submission will then be reviewed (at least) once more by the reviewers until they endorse your work for publication.

### Publication phase

The final phase is about making you're paper formally ready for publication. Apart from a potentially necessary stylistic reformatting, as requested by the editor, **you** should archive the final version of your work (paper + code) and use a service like [zenodo](https://zenodo.org/) to obtain a permanent DOI for it (which you should then post into the review GitHub-issue).

Finally, it's our turn to push your paper over the line and actually publish it in the JuliaCon proceeding.

@def title = "Reviewer's guide"
@def hascode = true

# Review Guidelines and Process

The role of reviewers is to ensure the quality of the content associated with
JuliaCon including proceedings and extended abstracts.

## Conflict of interest

In any case of conflict of interest, the reviewer commits to withdraw from a
review and signal it to the organizers to find a replacement quickly.
See the [PNAS guidelines](https://www.pnas.org/page/authors/conflict-of-interest)
for a definition and examples. Conflicts of interest include any work or
authors with which the reviewer has "any association that poses or could be perceived
as a financial or intellectual conflict of interest" (PNAS guidelines above).

## Code of Conduct

The reviewer commits to reading and respecting the conference
[Code of Conduct](https://juliacon.org/2019/coc) in the assessment and all
communications during the review process.

If some content submitted to the Conference does not comply with the Code of Conduct,
the reviewer should refer it to the organizing committee.

## Submitted documents

Submitted work comes in two types: extended abstracts and full papers.
See the author guide for more information on both.

## Review comments

Each review should include a general recommendation from the following list:

- Accept as-is: no modification required on the document
- Minor modification request: some changes are required but are minor enough to be done in one round, they do not affect the core content of the paper.
- Major modification request: some changes are requested on some central aspects of the paper and will need to be checked in an additional round of review.

In any case other than an acceptation as-is, the reviewer should provide the author with a list of
comments they can use to improve their document for the next round, citing the corresponding parts
of the documents, they should in all comments be as specific as possible.

## Review process

The review process is similar to the [Journal of Open-Source Software](http://joss.theoj.org)
and takes place in a dedicated GitHub issue (in [this repository](https://github.com/JuliaCon/proceedings-review/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc)).

### Checklist
A reviewer checklist is generated for each reviewer of the paper.
A box should be checked only once the reviewer considers that the criterion is met by the work presented.

**Note**: the checklist is only meant as a general guide for reviewers and does not capture
subject-specific best practices or notation consistency. The reviewer should feel free
to indicate what they consider should be edited in the submitted work.

### Different types of submission

Although typically the case, not all JuliaCon proceedings submissions are about presenting new (versions of) Julia packages. Instead, they might showcase an application use case, present a new feature added to an established package, or compare (an aspect of) a Julia package to the tools available in another programming language. In these cases, the review should be reasonably adapted to the character of the submission. For example, it might make sense to focus more on the paper (e.g. check wether the presentation or examples can be improved etc.) than strictly checking the code repository from a software development perspective. Questions like "Is there enough documentation?" or "Is there a LICENSE file?" might not make too much sense for some of these submission and you are free to take some liberty in deciding what are relevant points to check and improve as part of the review process.

(Note that this in contrast to JOSS, which focuses on software packages, applications, and libraries only and therefore doesn't allow these types of submissions in the first place.)
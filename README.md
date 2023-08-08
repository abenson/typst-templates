# Templates for Use with Typst

SPDX-License Identifier: Unlicense

These files are meant to be used with Typst v`0.7.0`.  They can be made to work
with older versions, though. I believe the only thing I'm using from v`0.7.0`
currently is `float:true`.

## Status

The goal is to have parity with the old Pandoc templates I had. Currently, I
have most of the old `work` template implemented, named `report`, but the
`work-plain` template is fully implemented.  They were combined in a single file
since they share several parts.

- [x] `work` => `classified/report`
- [x] `work-plain => `classified/simple`
- [ ] `mla`
- [ ] `memo`
- [ ] `letter`; I may borrow and tweak Typst's `letter` template

I may also adapt some of their other templates to my liking.

- [ ] `book`

I also intend to make my own presentation/briefing template.

- [ ] `presentation`

## Typst

I used to have a workflow based around [Pandoc](https://pandoc.org/). It allowed
me to write in Markdown and generate pretty PDFs using Pandoc's [template
system](https://github.com/abenson/custom-pandoc-templates/).

It's major drawback, for me, was an intermediary step that involved LaTeX.
TeXLive is huge, cumbersome, and on some of my smaller systems, such as my
Chromebook or ancient PowerBook, disk space is a limited commodity.

I began looking for a replacement, settling on reStructuredText and
[Rinoh](https://www.mos6581.org/rinohtype/) for a very short period of time,
until I found Typst.

[Typst](https://typst.app) is a typesetting framework similar to TeX and LaTeX,
but much smaller and with a newly designed language. Also, it borrows a lot of
inline formatting from other frameworks, such as `_italics_` and `*bold*`, which
make it easy to work with quickly.

## Setup

Simply clone this repo:

    $ git clone https://github.com/abenson/typst-templates

and then link to it from your documentation project:

    $ ln -s ~/path/to/typst-templates templates

Once there, you can use the templates in your own documents.

    #import "templates/manuscript.typ": manuscript
    #show: manuscript.with(
    <...>

Remember that assets, like the bibliography, logo, and other files, can be
included using using `/file.ext`; path will be relative to the file being
compiled. `file.ext`, without the leading `/`, will be relative from this
directory.

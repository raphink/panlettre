# General

This projects aims to provide an easy way to write French-speaking letters using `pandoc` and `lettre.cls`.

# Format

You can write the letters using Markdown (like the provided example, `foobar_exemple.md`, or reStructuredText).

Simply follow these instructions:

- Edit `default.ins` to fit your settings. Set `\name{}` there if you want a fix sender's name;
- Each document should be named with the pattern `recipient_whatever.extension`, where `recipient` is the name of a file in the `addresses/` directory, containing the recipient's address, typeset in LaTeX;
- The (optional) document title will be used as the letter's subject;
- The (optional) document author will be used as the signature. You should provide this value if you haven't set it with `\name{}` in `default.ins`;
- The first "section" heading in the document will be used as the opening;
- The second (and last) "section" heading in the document will be used as the closing;
- Any other top-level section heading will be ignored.

# Generating documents

You can generate LaTeX or PDF documents using the `panlettre` command. For example:

    $ panlettre foobar_exemple.md foobar_exemple.pdf

will generate a PDF, using the Markdown document as a source. Note that there must be a file named `addresses/foobar`, containing the address of the `foobar` recipient.

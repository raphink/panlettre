# General

This projects aims to provide an easy way to write French-speaking letters using `pandoc` and `lettre.cls`.

# Format

You can write the letters using Markdown (like the provided example, `foobar_exemple.md`, or reStructuredText).

## Letter's object (optional)

The object of the letter is set with the `title` field (the first `%` field in Markdown).
If left empty, the letter's object will not be printed.

## Recipient's address

The recipient is set with the `author` field (the second `%` field in Markdown). If it needs to span on several lines, use trailing spaces in Markdown.

## Date (optional)

The date can be set using the `date` field (the third `%` field in Markdown). Unless specified, it will default to the day's date.

## Signature

The signature is set using the first section heading (the first `#` field in Markdown).

## Opening

The opening is set using the second section heading (the second `#` field in Markdown).

## Closing

After the main body, the closing is set using the third section heading (the third `#` field in Markdown).

# Generating documents

You can generate LaTeX or PDF documents using the `panlettre` command. For example:

    $ panlettre foobar_exemple.md foobar_exemple.pdf

will generate a PDF, using the Markdown document as a source.

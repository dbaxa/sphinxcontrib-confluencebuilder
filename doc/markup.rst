markup
======

The following outlines the reStructuredText_ / Sphinx_ markup explicitly supported
by this extension. The intent of this extension is to support as much markup as
possible that can be rendered on a Confluence instance. Below will identify
markup that has been tested, planned to be implemented in the future or is not
compatible with Confluence.

standard
--------

.. keywords | partial, planned, prospect, unplanned, unsupported

====================== ============= =====
type                   status        notes
====================== ============= =====
admonitions            completed     - `reStructuredText Admonitions`_
bibliographic fields   planned       - `reStructuredText Bibliographic Fields`_
block quotes           partial       - `reStructuredText Block Quotes`_
                                     - Multi-line block quotes may not work as
                                       expected.
bullet lists           completed     - `reStructuredText Bullet Lists`_
centered               unsupported   - `Sphinx Centered`_
citations              completed     - `reStructuredText Citations`_
code                   partial       - `Sphinx Code Markup`_
                                     - code-block options ``emphasize-lines``
                                       and ``lines`` as well as highlight option
                                       ``linenothreshold`` are ignored due to
                                       incompatibilities with Confluence's code
                                       block macro.
                                     - Highlighting is limited to languages
                                       defined by the Confluence instance (see
                                       `code block macro`_).
                                     - Pending work to validate/improve code
                                       block options ``caption``, ``encoding``
                                       and ``pyobject``.
compound paragraph     completed     - `reStructuredText Compound Paragraph`_
container              prospect      - `reStructuredText Container`_
definition lists       completed     - `reStructuredText Definition Lists`_
deprecated             completed     - `Sphinx Deprecated`_
enumerated lists       completed     - `reStructuredText Enumerated Lists`_
                                     - Only auto-enumerator lists (``#``) are
                                       supported.
epigraph               prospect      - `reStructuredText Epigraph`_
footnotes              completed     - `reStructuredText Footnotes`_
glossary               partial       - `Sphinx Glossary`_
                                     - Visually renders definitions; references
                                       to entries not yet supported.
highlights             prospect      - `reStructuredText Highlights`_
hlist                  unsupported   - `Sphinx Horizontal List`_
hyperlink targets      completed     - `reStructuredText Hyperlink Targets`_
images                 prospect      - `reStructuredText Images`_
list table             partial       - `reStructuredText List Table`_
                                     - Argument ``title`` not yet supported.
                                     - Options not supported: ``align``,
                                       ``header-rows``, ``stub-columns`` and
                                       ``widths``.
literal blocks         completed     - `reStructuredText Literal Blocks`_
math                   unplanned     - `reStructuredText Math`_
option lists           planned       - `reStructuredText Option Lists`_
production list        planned       - `Sphinx Production List`_
pull-quote             prospect      - `reStructuredText Pull-Quote`_
raw                    planned       - `reStructuredText Raw Data Pass-Through`_
rubric                 completed     - `Sphinx Rubric`_
sections               completed     - `reStructuredText Sections`_
tables                 partial       - `reStructuredText Tables`_
                                     - Spanning not supported at this time.
toctree                partial       - `Sphinx TOC Tree Markup`_
                                     - Pending work to validate/improve toctree
                                       options ``caption`` and ``numbered``.
transitions            completed     - `reStructuredText Transitions`_
versionadded           completed     - `Sphinx Version Added`_
versionchanged         completed     - `Sphinx Version Changed`_
====================== ============= =====

*(note: directive options "class" and "name" are ignored)*

extensions
----------

This extension has currently no official support for other Sphinx extensions at
this time.

There is plans to support the following extensions in the future:

 - `sphinx.ext.autodoc`_ (`Issue 51`_)

.. _Issue 51: https://github.com/tonybaloney/sphinxcontrib-confluencebuilder/issues/51

other
-----

If a markup type and/or extension is not listed in the above, is not working as
expected or brings up another concern, feel free to bring up an issue:

    | Atlassian Confluence Builder for Confluence - Issues
    | https://github.com/tonybaloney/sphinxcontrib-confluencebuilder/issues

.. _code block macro: https://confluence.atlassian.com/confcloud/code-block-macro-724765175.html
.. _reStructuredText: http://docutils.sourceforge.net/rst.html
.. _reStructuredText Admonitions: http://docutils.sourceforge.net/docs/ref/rst/directives.html#admonitions
.. _reStructuredText Bibliographic Fields: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#bibliographic-fields
.. _reStructuredText Block Quotes: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#block-quotes
.. _reStructuredText Bullet Lists: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#bullet-lists
.. _reStructuredText Citations: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#citations
.. _reStructuredText Compound Paragraph: http://docutils.sourceforge.net/docs/ref/rst/directives.html#compound-paragraph
.. _reStructuredText Container: http://docutils.sourceforge.net/docs/ref/rst/directives.html#container
.. _reStructuredText Definition Lists: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#definition-lists
.. _reStructuredText Enumerated Lists: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#enumerated-lists
.. _reStructuredText Footnotes: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#footnotes
.. _reStructuredText Epigraph: http://docutils.sourceforge.net/docs/ref/rst/directives.html#epigraph
.. _reStructuredText Highlights: http://docutils.sourceforge.net/docs/ref/rst/directives.html#highlights
.. _reStructuredText Hyperlink Targets: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#hyperlink-targets
.. _reStructuredText Images: http://docutils.sourceforge.net/docs/ref/rst/directives.html#images
.. _reStructuredText List Table: http://docutils.sourceforge.net/docs/ref/rst/directives.html#list-table
.. _reStructuredText Literal Blocks: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#literal-blocks
.. _reStructuredText Math: http://docutils.sourceforge.net/docs/ref/rst/directives.html#math
.. _reStructuredText Option Lists: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#option-lists
.. _reStructuredText Pull-Quote: http://docutils.sourceforge.net/docs/ref/rst/directives.html#pull-quote
.. _reStructuredText Raw Data Pass-Through: http://docutils.sourceforge.net/docs/ref/rst/directives.html#raw-data-pass-through
.. _reStructuredText Sections: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#sections
.. _reStructuredText Tables: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#tables
.. _reStructuredText Transitions: http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html#transitions
.. _Sphinx: http://sphinx-doc.org/
.. _Sphinx Centered: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-centered
.. _Sphinx Code Markup: http://www.sphinx-doc.org/en/stable/markup/code.html
.. _Sphinx Deprecated: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-deprecated
.. _Sphinx Glossary: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-glossary
.. _Sphinx Paragraph-level Markup: http://www.sphinx-doc.org/en/stable/markup/para.html
.. _Sphinx Production List: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-productionlist
.. _Sphinx Horizontal List: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-hlist
.. _Sphinx Rubric: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-rubric
.. _Sphinx TOC Tree Markup: http://www.sphinx-doc.org/en/stable/markup/toctree.html
.. _Sphinx Version Added: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-versionadded
.. _Sphinx Version Changed: http://www.sphinx-doc.org/en/stable/markup/para.html#directive-versionchanged
.. _sphinx.ext.autodoc: http://www.sphinx-doc.org/en/stable/ext/autodoc.html

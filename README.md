# Luv Unofficial Docs

### Here you can find unofficial documentation on using [Luv](https://github.com/luvit/luv).

[![Documentation Status](https://readthedocs.org/projects/luv/badge/?version=latest)](http://luv.readthedocs.org/en/latest/?badge=latest)

Latest generated docs can be found at: [http://luv.readthedocs.org/](http://luv.readthedocs.org/)

__Please feel free to contribute to missing spots, or incorrect assumptions and/or information.__

To contribute, just clone the repo, edit, and request a pull.

## Development

[MkDocs](http://www.mkdocs.org/user-guide/writing-your-docs/) is the formatting engine/theme.

__Not all options from MkDocs work on the readthedocs.org site. Extensions do work however.__

### Extensions

You can use the following extensions with MkDocs:

codehilite - Hilite your code with three back-ticks and language id, as shown:

<pre>
```lua
--Some code
```
</pre>

callouts (admonition) - Create call-out boxes. Each one uses a different color.

<pre>
!!! note "A Note"
    Here is some informative text.

!!! warning ""
    This is a block, without a title, which supresses rendering the header.

    You can have multi-line, on the same indetation level.

!!! danger "Don't Do It!"
    If you do this, your computer will explode.
</pre>

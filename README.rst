Syntax highlighting
===================

Github knows to syntax highlight ``test_two``, but not ``test_one``.

The difference is test_one has extra arguments after the ``#!/usr/bin/env python``
in the shebang.

I use this pattern in my repo over at https://github.com/delfick/photons-core/tree/master/scripts
where I don't want to surface the fact that some of the scripts are python and
have the .py extension. I need the complicated shebang so that when you execute
the scripts as it's own thing, you don't need to know to use the python from
the virtualenv to run them.

To run the scripts in this repo you just do::

    $ ./test_one
    $ ./test_two

They both do the same thing, but test_one uses a virtualenv that gets created
when you run it, while test_two uses your system python

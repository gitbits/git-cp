git-cp
======

Synopsis
--------

* git-cp - a convenient only subcommand for git that does cp(1) and git-add(1)

* git-touch - git-add new empty files with automatic directory creation

* git-untouch - undo git-touch

Usage
-----

    git cp [options] <source>... <destination>

        -v, --verbose         be verbose
        -n, --dry-run         dry run
        -f, --force           force move/rename even if target exists
        -k                    skip move/rename errors

    git touch <filename>...

        -v, --verbose         be verbose
        -n, --dry-run         dry run
        -k                    skip create errors

    git untouch <filename>...

        -v, --verbose         be verbose
        -n, --dry-run         dry run
        -k                    skip any error

Description
-----------

`git-cp(1)` is written in Perl, which many git subcommands already
use, to avoid extra dependency.

It calls `git-mv(1)` internally to borrow its checking/parsing
abilities, so if the output message format changes `git-cp(1)` may
stop working.

`git-touch(1)` provides a convenient way to create one or more empty
files and get them staged.  If a specified file already exists, it
just adds the path to the index using `git add -N file`.

`git-untouch(1)` undoes what `git-touch(1)` has done.

License
-------

Copyright (c) 2012-2015 Akinori MUSHA.

Licensed under the 2-clause BSD license.  See `LICENSE.txt` for
details.

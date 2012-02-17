git-cp
======

Synopsis
--------

* git-cp - a convenient only subcommand for git that does cp(1) and git-add(1)

* git-touch - git-add new empty files with automatic directory creation

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

Description
-----------

`git-cp(1)` is written in Perl, which many git subcommands already
use, to avoid extra dependency.

It calls `git-mv(1)` internally to borrow its checking/parsing
abilities, so if the output message format changes `git-cp(1)` may
stop working.

`git-touch(1)` provides a convenient way to create one or more empty
files and stage them.

License
-------

	Copyright (c) 2012 Akinori MUSHA
	
	All rights reserved.
	
	Redistribution and use in source and binary forms, with or without
	modification, are permitted provided that the following conditions
	are met:
	1. Redistributions of source code must retain the above copyright
	   notice, this list of conditions and the following disclaimer.
	2. Redistributions in binary form must reproduce the above copyright
	   notice, this list of conditions and the following disclaimer in the
	   documentation and/or other materials provided with the distribution.
	
	THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
	ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
	IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
	ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
	FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
	DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
	OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
	HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
	LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
	OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
	SUCH DAMAGE.

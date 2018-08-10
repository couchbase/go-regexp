This repository is a fork of the golang regexp package, to allow
access to some internal fields (namely, the syntax parse tree).

Initialization steps...

    $ mkdir go-regexp && cd go-regexp
    $ git init .
    $ git remote add github https://github.com/golang/go.git

Then, these were the steps to pick a golang release to fork...

    $ git remote update
    $ git reset --hard go1.9.6
    $ git describe --all --long
    tags/go1.9.6-0-g20f58c6075

To get the regexp package to the top-level dir and remove other parts...

    $ git mv src/regexp/ .
    $ git rm -rf api doc lib misc src test
    $ git rm -rf regexp/syntax/ regexp/testdata favicon.ico robots.txt

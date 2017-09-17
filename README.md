# pyrestic - frob restic repositories with python

## Background

Lately I've been doing a lot of work with the
[restic](https://github.com/restic/restic) backup program. When dealing with
backups, I worry about long term stability and accessability of the content
I'm storing. The restic code is freely available, and the documentation 
contains a rather complete description of the restic repository format. For
something as important as backups, however, I don't fully trust something
until I can pull a file out with my bare hands, so to speak. I also love
Go, but I generally can throw things together more quickly with Python.
So, to both exercise and soothe my mind, enough Python to be able to tear
something out of a native restic repository.

## Caveat

This is not meant to be a replacement for restic, or to even be all that
usable. It's mostly a proof-of-concept.

**DO NOT TRUST MY CRYPTO**

If you use this code to actually try to encrypt something, or as a guide
to actually using crypto, **_YOU ARE AN IDIOT_**.

Now that we've got that out of the way, crypto coding is fraught with perils
which are doubly exacerbated by amateurs (read: me). While it is the stated
goal of this project to be able to successfully decrypt objects from a real
restic repository, the fact that it can (to the extent that it can) is almost
approaching accidental. If you want real crypto, use real crypto software
or hire an engineer who can make it for you.

## Test repository

A test restic repository is located in the directory `test_repo`. It has
three passphrases:

* `The hidden stone ripens fast, then laid bare like a turnip`
* `can easily be cut at last, but even then the danger isn't past.`
* `That man lives best who's fain, to live half mad, half sane.`

For convenience, these passphrases are located in the files `pass1`,
`pass2` and `pass3` in the top level git repo.

The test repository was created with restic 0.7.2.

## Canonical Location

This code's canonical public git repository is
https://kula.tproa.net/code/pyrestic.git/

It may also be found at https://github.com/kula/pyrestic/

## License

This git repository, except as otherwise noted, is copyright and licensed under
the terms of the `LICENSE` file located at the top of this repository.

I lay no claim or license to the directory `test_repo`

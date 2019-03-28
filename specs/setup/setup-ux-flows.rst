Setup UX flow
=============

High-level experience of a user setting up radicle locally for the first time.

Install
-------

::

    $ brew install radicle
    ==> Installing radicle 
    ==> Downloading https://homebrew.bintray.com/bottles/radicle-11.1.mojave.bottle.tar.gz
    ==> Pouring radicle-11.1.mojave.bottle.tar.gz
    ==> Caveats
    Great success!!!

    To see if radicle is installed properly, run:
      rad --version

    To get started with radicle, run:
      rad setup
    ==> Summary
    🍺  /usr/local/Cellar/radicle/11.1: 3,548 files, 40.3MB


Setup
-----

::

    $ rad setup
    => Creating config directory in ~/.config/radicle
    => Creating personal keypair in ~/.config/radicle/keys/<HASH>.pub
    => Your keypair: <HASH>
    => Configuring and starting ipfs node for radicle
    => Radicle ipfs daemon running
    => What template would you like to use?
      basic language stack
    > code collaboration stack
    => Setting up code collaboration stack
    => Installing: github.com/oscoin/radicle-git
    => Installing: github.com/oscoin/radicle-git-diff
    => Setup complete!
    => To get familiar with radicle code collabration stack, visit:
      https://radicle.xyz/code-collaboration/tutorial

    => If you just want to see a list of available commands, run:
      rad git --help
      rad diff --help


Tutorial
--------

.. TODO(xla): Address the specifications of the tutorial as soon as all
   subcommands are working and in place.

+ understanding of git, link to tutorial
+ init an exisiting or new repo
+ publish to radicle
+ contribute to someone's repo
+ see and merge a diff on my repo


Refer to the `diff flow <../diff/diff-ux-flows.rst>`_

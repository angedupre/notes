Project UX flows
================

The following flows describe high-level interactions a user can perform the
with the radicle **project** app.

Create a new project for code collaboration
-------------------------------------------
I create a new empty directory which will be used as the foundation of my
project.

::

   $ mkdir acme
   $ cd acme

Initialize it as radicle project and choose code collaboration.

::

  $ rad project init
  ? What's the name of your project (Default: acme)? acme
  ? Briefly describe your project? This is my description
  ? What kind of repository would you like to use?
  1. New peer-to-peer repository (git-ipfs **EXPERIMENTAL**)
  2. Add your own remote (e.g.: github / gitlab / ...)
      (see radicle.xyz/docs/storage for more info)

If you choose option 1

::

  Initialised empty Git repository in ~/acme/.git
    adding "origin" remote: ipfs://QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG
  => Assembled rad-issues machine
  => Assembled rad-diff machine

  Your project id is 554179. See the id of your project by running:
    rad project show-id

  Run --help to get started
    rad issue --help
    rad diff --help

If you choose option 2

::

  Initialised empty Git repository in ~/acme/.git
  => Assembled rad-issues machine
  => Assembled rad-diff machine

  Your project id is 554179. See the id of your project by running:
    rad project show-id

  Run --help to get started
    rad issue --help
    rad diff --help

  To add you own remote, run:
    git remote add <REMOTE NAME> <REMOTE-URL>


Share my project id out-of-band
-------------------------------
Quickly extract my project id to make it publicly available or share directly
with another person.

::

   $ rad project show-id
   <PROJECT-ID>

.. Fork a project not owned by me
.. ------------------------------
.. Create a personal copy and locally check it out.

.. ::

..    $ rad project fork <PROJECT-ID>
..      Cloning into 'acme'...
..      remote: Enumerating objects: 70, done.
..      remote: Counting objects: 100% (70/70), done.
..      remote: Compressing objects: 100% (40/40), done.
..      remote: Total 1472 (delta 30), reused 60 (delta 22), pack-reused 1402
..      Receiving objects: 100% (1472/1472), 4.71 MiB | 1.59 MiB/s, done.
..      Resolving deltas: 100% (546/546), done.
..      adding "origin" remote: ipfs://QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG
..      adding "upstream" remote: ipfs://QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz2948asjdla
..      pushing fork to origin
..    o Copied rad-issue machine
..    o Copied rad-diff machine

..    Your project id is <FORK-PROJECT-ID>. See the id of your project by running:
..      rad project show-id

..    To be able to contribute to the upstream project, run:
..      rad diff propose --upstream <git-object-id>


Collaborate on another project
------------------------------
Given I obtaine the project id out-of-band I can checkout the project so I can
act on it locally.

::

   $ rad project checkout <PROJECT-ID>
     Cloning into ./acme/
     remote: Enumerating objects: 70, done.
     remote: Counting objects: 100% (70/70), done.
     remote: Compressing objects: 100% (40/40), done.
     remote: Total 1472 (delta 30), reused 60 (delta 22), pack-reused 1402
     Receiving objects: 100% (1472/1472), 4.71 MiB | 1.59 MiB/s, done.
     Resolving deltas: 100% (546/546), done.
     adding "origin" remote: ipfs://QmYwAPJzv5CZsnA625s3Xf2nemtYgPpHdWEz79ojWnPbdG

   Created ./adcme/.rad-config
   To list the project's issues, run:
     rad issue list


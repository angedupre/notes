Project overview
=================

A **project** is an RSM whose state contains collection of related RSMs.
The more important example is RSMs related to a particular repository (e.g.,
issues, revisions, and the repo itself); but we could also for example have a
project that points to all projects of a user.

In addition to providing a discovery mechanism, projects make it easier to
relocate sub-RSMs. The idea is that owners would never give away keys to the
project itself, though they may choose to give away keys to sub-RSMs (e.g.,
self-host them on a server, or have it hosted by a service). If they then
choose to move to a different hosting system, all they have to do is update the
project RSM.

Since the project RSM changes rarely, and is intended to be written by only
one person -- the owner --, it can be managed entirely on one's personal
computer.

Format
------

This section describes the **radicle** formats and API for the project RSM.
CLI interactions will be described in different documents.

Each RSM has minimally the following format:

::

   { :id <url>
     :type <type>
   }

The known RSMs can be queried with `list-rsms`:

::

    (list-rsms)
       >> [ { :id <url1> :type :rad-repo }
            { :id <url2> :type :rad-issues }
            { :id <url3> :type :rad-revisions }
          ]


New rsms can be added:

::

   (add-rsm { ... }) ;; signed and nonced transaction

Modified:

::

   (modify-rsm { <old> } { <new> }) ;; signed and nonced transaction


Or deleted:

::

   (delete-rsm { ... }) ;; signed and nonced transaction

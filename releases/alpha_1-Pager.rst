α-release 1-Pager
=================

**2019-01-15**

TL;DR
-----

The focus is on a rudimentary code collaboration flow outlined in the following
document which most of you have seen already: `diff flow <../specs/diff/diff-ux-flows.rst>`_

From a user perspective, we're splitting things up in what we call apps where
each app is a bundle of functionality, with a UI (with focus on the terminal
for now) and a radicle RSM. The RSM has local storage, IPFS input storage, and
radicle as the state transition function.

Then we'll create a brand and homepage under `radicle.xyz <http://radicle.xyz>`_ where
we highlight this functionality, explain how to use it and onboard potential
users to the stack.

Status Overview
---------------

+-------------------+---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
| Topic             | Components                | Owner  | State        | Spec                                                                                                       | Repo                                                                  |
+===================+===========================+========+==============+============================================================================================================+=======================================================================+
| `Apps`_           | Project/Repo              | Julian | **PLANNING** | `UX flows <../specs/repo/repo-ux-flows.rst>`_                                                              | /                                                                     |
|                   |                           |        |              |                                                                                                            |                                                                       |
|                   |                           |        |              | `PR <https://github.com/oscoin/docs/pull/19>`_                                                             |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | Diff                      | Merle  | **WIP**      | `UX flows <../specs/diff/diff-ux-flows.rst>`_                                                              | `radicle <https://github.com/oscoin/radicle>`_                        |
|                   |                           |        |              |                                                                                                            |                                                                       |
|                   |                           |        |              | `PR <https://github.com/oscoin/radicle/pull/370>`_                                                         |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | Setup                     | xla    | **PLANNING** | `UX flows <../specs/setup/setup-ux-flows.rst>`_                                                            | /                                                                     |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | Issue *optional*          | Julian | **WIP**      | `UX flows <../specs/issue/issue-ux-flows.md>`_                                                             | `radicle <https://github.com/oscoin/radicle>`_                        |
+-------------------+---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `Infrastructure`_ | git-remote-ipfs           | Kim    | **DONE**     | /                                                                                                          | `ipfs <https://github.com/oscoin/ipfs/tree/master/git-remote-ipfs>`_  |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | radicle-p2p               | Thomas | **WIP**      | `Machine Backend <https://github.com/oscoin/radicle/blob/master/rfcs/0001-machine-backend-interface.rst>`_ | `radicle <https://github.com/oscoin/radicle>`_                        |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+                                                                       |
|                   | IPFS daemon               | Thomas | **WIP**      | `UX flows <../specs/ipfs/ipfs-ux-flows.rst>`_                                                              |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+                                                                       |
|                   | Radicle Daemon            | James  | **WIP**      | `RFC <https://github.com/oscoin/radicle/blob/rfc/daemon/rfcs/0003-radicle-daemon.rst>`_                    |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | Platform                  | Alexis | **PLANNING** | /                                                                                                          | /                                                                     |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | App management *optional* | xla    | **PLANNING** | /                                                                                                          | /                                                                     |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
|                   | rad.xyz deploys           | xla    | **PLANNING** | /                                                                                                          | /                                                                     |
+-------------------+---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+
| `radicle.xyz`_    | Brand                     | Sam    | **WIP**      | `Identity PR <https://github.com/oscoin/docs/pull/18>`_                                                    | `docs <https://github.com/oscoin/docs>`_                              |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+                                                                       |
|                   | Community Strategy        | Sam    | **Done**     | `Strategy <../strategy/community-strategy.rst>`_                                                           |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+                                                                       |
|                   | Content Strategy          | Sam    | **WIP**      | `Spec <https://docs.google.com/document/d/1rg4DZtqg3KZ5WCbhbPxmaK9rRTiRvqcSlPU2CqbExo0/edit?usp=sharing>`_ |                                                                       |
|                   +---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+                                                                       |
|                   | Information Architecture  | Julien | **DONE**     | `Spec <http://reflective-toy.surge.sh>`_                                                                   |                                                                       |
+-------------------+---------------------------+--------+--------------+------------------------------------------------------------------------------------------------------------+-----------------------------------------------------------------------+

Apps
----

+ Project/Repo [Julian]

  *Hosting of git repositories on ipfs.*

  * Setup of main project machine with links to machine IDs
  * Repository initialization
  * Diff initialisation
  * Issues initialisation

+ Diff [Merle]

  *Sharing code contributions for a git repo.*

  * Propose changes
  * List proposed changes on my repo
  * Show a proposed change
  * Accept/reject proposals

+ Setup [xla]

  *Initial radicle setup for a user.*

  * Setup radicle operational
  * Onboard users to app management

+ Issues [Julian] *optional*

  *Issues with comments around a project.*

  * Create issues
  * Discuss issues
  * Open and close issues


Infrastructure
--------------

Additionally, these apps rely on infrastructure, the core of which is the
replication layer built on IPFS, which includes a couple of components
necessary for the apps to be built, as well as CLI infrastructure.

+ git-remote-ipfs [Kim]

  * Transparent use of ipfs as git remote
  * Git remote interaction (push/pull/clone) via a git-remote-helper

+ radicle-p2p (Replication layer) [Thomas]

  * Storage of radicle chains on IPFS with a well specified data representation
  * Stable chain IDs on top of IPNS

+ IPFS daemon [Thomas]

  * Specialised operation of an IPFS daemon to serve the radicle use-case

+ Daemon [James]

  * Local state materialization of radicle chains, given an IPFS hash (CLI)
  * Local state perspective (CLI)
  * Enables submissions to other peoples machines
  * Easier replication
  * Performance gains for the cli and caching

+ Platform [Alexis]

  * CLI integrations
  * Configuration formats locations and sharing
  * User identifier format
  * Repo identifier format
  * Packaging and distribution of radicle
  * Distribution and storage of .rad files

+ App management [xla] *optional*

  * App installation
  * App upgrades
  * CLI code upgrade

+ rad.xyz deploys [xla]

  * https for radicle.xyz
  * static site generation from markup files
  * support for a blog

radicle.xyz
-----------

+ Brand

  Brand work is well on the way, check out the progress in Roon's presentations `here <https://github.com/oscoin/docs/pull/18>`_

+ Community Strategy

  Community strategy work is mapped out `here by Sam <../strategy/community-strategy.rst>`_

+ Content Strategy

  Cory, Sam, Ele and Julien are collaborating over the content of the website in this `spec <https://docs.google.com/document/d/1rg4DZtqg3KZ5WCbhbPxmaK9rRTiRvqcSlPU2CqbExo0/edit?usp=sharing>`_ This follows the Information Architecture that Ele and Julien defined and layed out in this `prototype <http://reflective-toy.surge.sh>`_

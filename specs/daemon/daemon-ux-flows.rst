Daemon UX flows
===============

This document breaks down the user expectations for the daemon sub-command,
which is reserved for advanced users who are comfortable with process
management and have an understanding of the underlying components of the
radicle system.

Running the ipfs daemon
-----------------------
I want to start the custom-configured ipfs daemon which is a prerequisite for
radicle to work.

::

   $ rad daemon ipfs
   Initializing daemon...
   API server listening on /ip4/127.0.0.1/tcp/9301
   Gateway server listening on /ip4/127.0.0.1/tcp/9302

In case that the ipfs binary is missing the user gets presented an error and help text to resolve the issue.

::

   $ rad daemon ipfs
   ERROR: Unknown command: ipfs
   Follow the instructions here: https://docs.ipfs.io/introduction/install/

Running the radicle daemon
--------------------------
I want to start the radicle daemon which the cli will access locally.

::

   $ rad daemon radicle
   INFO   Following as reader id=12D3KooWHSyxPrSnFNEHbq6CurdUVgqorVwBNMgx4S5HvNBWPQo9
   INFO   Start listening port=8910
   INFO   Refreshed as reader id=12D3KooWHSyxPrSnFNEHbq6CurdUVgqorVwBNMgx4S5HvNBWPQo9 n=0

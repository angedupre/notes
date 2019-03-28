Issues user flow
================

These flows describe how users can manage and collaborate on issues similar to
Github but built on radicle.

We assume that there is one radicle machine for a group of issues, e.g. all
issues belong a project, which has a code repository.

Issues on a machine are uniquely identified by a monotonically increasing
number starting with 1.

See existing issues
-------------------
To get an understanding of what the open issues are for a project I'm going to
list them.

::

  $ rad issue list
  state    #    title                    author        updated
  open     32   can't log in             juliendonck   2019-01-25T13:27
  open     23   some title               cloudhead     2019-01-25T13:27
  closed   12   why doesn't this work?   xla           2019-01-25T13:27

To get a subset of issues presented, for example the open ones I can call the
list command with an option.

::

  $ rad issue list --state open
  state    #    title                    author        updated
  open     32   can't log in             juliendonck   2019-01-25T13:27
  open     23   some title               cloudhead     2019-01-25T13:27


Creating an issue
-----------------
We assume that we operate in the context of an already checked out project.

The following command opens `$EDITOR` to edit a temporary file. Once the editor
exits we use the content of that file to create the issue. The first line is the
title, the rest is the body. The command outputs the number of the issue
created.

::
  $ rad issue new


In the editor you'll see this template you need to edit:

::

  ;; Issue template. An empty or invalid value will abort.
  {:title      "Pick a title"
  :body       "Pick a body"
  :labels     []
  }

After you've saved that file and closed the editor you'll see:

::

  $ rad issue new
  Created issue #33 in acme

View the issue
--------------
This will show the output of the issue with the provided number and all the
comments in it, the user will be able to use tools like less to make the output
more digestable.

::

  $ rad issue show <ISSUE-NUMBER>
  # Issue 0: Implement issue command

  created by MeBrei [2019-02-12T10:46:05Z]

  **State:** open
  **Labels:** []

  This is the body of the issue. Bla bla bla I've got an issue!!

  Comments
  --------

  ### MeBrei [2019-02-12T10:46:34Z]

  commenting

  ### MeBrei [2019-02-12T10:54:49Z]

  bla

Comment on an issue
-------------------
I provide a body and the correct issue number to comment on an issue.

::

  $ rad issue comment #33 'I have doubts'
  Commented on issue 33 in docs

Resolve an issue
----------------
Assuming an issue has been addressed, potentially with a code contribution, the
maintainer should be able to close it.

::

  $ rad issue close 33
  Issue 33 closed

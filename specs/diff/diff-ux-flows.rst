Diffs user flow
===============

The following flows are an attempt to capture the high-level interactions
a user can perform given a minimal set of functionality is provided in order to
share and collaborate on code. It is assumed the user has a working setup of
radicle and the git and diff app installed.

Propose a diff
--------------

Someone shared a rad repo id/project id with me. (This part needs changes)

::

   $ rad repo fork <REPO-ID/PROJECT-ID>
   Cloning into 'acme'...
   remote: Enumerating objects: 70, done.
   remote: Counting objects: 100% (70/70), done.
   remote: Compressing objects: 100% (40/40), done.
   remote: Total 1472 (delta 30), reused 60 (delta 22), pack-reused 1402
   Receiving objects: 100% (1472/1472), 4.71 MiB | 1.59 MiB/s, done.
   Resolving deltas: 100% (546/546), done.
   => adding "origin" remote: <CLONED-REPO-URL>
   => adding "upstream" remote: <REPO-URL>
   => pushing fork to origin
   => You can always see the id of your repo by running:
      rad repo show-id

And I'm going to make a change.

::

   $ cd acme
   $ vi main.c

Confirm and commit my changes.

::

    $ git status --short
    M main.c
    $ git commit -m 'Super dope feature' main.c
    [master 3f9e302] Super dope feature
      1 file changed, 398 insertions(+)
      create mode 100644 main.c

Now I want to propose my diff to upstream using the git object id of the last
commit (`3f9e302`).

::

    $ rad diff propose 3f9e302
    => Proposing <DIFF-NUMBER> to <REPO-ID>

Validate that my latest diff is published.

::

    $ rad diff list
    state      #   commit                           author        updated
    rejected   3   Commit message                   cloudhead     2019-01-25T13:27
    pending    2   Super dope feature               juliendonck   2019-01-22T13:27
    accepted   1   New way of importing something   jkarni        2019-01-25T13:27

Or retract my proposed diff if I changed my mind.

::

    $ rad diff retract <DIFF-NUMBER>
    => Diff <DIFF-NUMBER> has been successfully retracted

See a diff on my repo
---------------------

By navigating to my repo.

::

    $ cd acme/

List all existing diffs for my repo. The list can be filtered by state by
appending any combination of `--filter-by-state`, `--state` or short `--s`
followed by one of `accepted`, `rejected`, `retracted` and `pending`.

::

    $ rad diff list --s pending --s accepted
    state      #   commit                           author        updated
    pending    2   Super dope feature               juliendonck   2019-01-22T13:27
    accepted   1   New way of importing something   jkarni        2019-01-25T13:27

To inspect a single diff.

::

    $ rad diff show <DIFF-NUMBER>
    From 3f9e302ef68c74251c49cd4d1bf17452b713620 Mon Sep 17 00:00:00 2001
    From: <SOMEONE-NAME> <SOMEONE-EMAIL>
    Date: Wed, 16 Jan 2019 10:35:58 +0000
    Subject: Super dope feature

    Description of the feature
    ---
    main.c | 398 +++++++++++++++++++++++++++++++++++
    1 file changed, 398 insertions(+)
    // ...

And accept if it looks good.

::

    $ rad diff accept <DIFF-NUMBER>
    => Merging proposal <DIFF-NUMBER> with master

Or reject it.

::

    $ rad diff reject <DIFF-NUMBER>
    => Diff <DIFF-NUMBER> has been rejected

Or add a general comment for clarification or to request a change.

::

    $ rad diff comment <DIFF-NUMBER> "Nice feature, but here is my comment..."
    => Added comment to Diff <DIFF-NUMBER>

*Improvement:* Inline code comments. (not included in the alpha release)

React to reviews of my diff
---------------------------

I inspect my diff to read the comment.

::

    $ rad diff show <DIFF-NUMBER>
    state      #   commit                           author        updated
    pending    2   Super dope feature               juliendonck   2019-01-22T13:27

    created at 2019-01-22T09:32:37Z

    From 3f9e302ef68c74251c49cd4d1bf17452b713620 Mon Sep 17 00:00:00 2001
    From: <MY-NAME> <MY-EMAIL>
    Date: Wed, 16 Jan 2019 10:35:58 +0000
    Subject: Super dope feature

    Description of the feature
    ---
    main.c | 398 +++++++++++++++++++++++++++++++++++
    1 file changed, 398 insertions(+)
    // ...
    Comments
    --------
    <MAINTAINERS-NAME> <created-at>
    Nice feature, but here is my comment...

And reply to it.

::

    $ rad diff comment <DIFF-NUMBER> "Re: comment"
    => Added comment to Diff <DIFF-NUMBER>

If I (as a contributer) try to accept it anyways, I get an error message. (WIP)

::

    $ rad diff accept <DIFF-NUMBER>
    => Only maintainers can accept diffs.

*Improvement:* Or update my diff with another commit. (WIP)

::

    $ rad diff update <DIFF-NUMBER> 9359fef
    => Adds the diff to the DIFF and updates modified-at

Merge a diff on my repo
-----------------------

I check on new and changed diffs that are pending and see that the contributer
reacted with a comment (*and possibly made updates*).

::

    $ rad diff list --s pending
    state      #   commit                           author        updated
    pending    2   Super dope feature               juliendonck   2019-01-22T13:27

I inspect the diff to read the comment.

::

    $ rad diff show <DIFF-NUMBER>
    (pending) [<SOMEONE-NAME>] 3f9e302 - Super dope feature | <DIFF-NUMBER>

    created at 2019-01-22T09:32:37Z

    From 3f9e302ef68c74251c49cd4d1bf17452b713620 Mon Sep 17 00:00:00 2001
    From: <SOMEONE-NAME> <SOMEONES-EMAIL>
    Date: Wed, 16 Jan 2019 10:35:58 +0000
    Subject: Super dope feature

    Description of the feature
    ---
    main.c | 398 +++++++++++++++++++++++++++++++++++
    1 file changed, 398 insertions(+)
    // ...
    Comments
    --------
    <MY-NAME> <created-at>
    Nice feature, but here is my comment...

    <SOMEONE-NAME> <created-at>
    Re: comment...

I checkout the diff locally in a branch for testing.

::

    $ rad diff checkout <DIFF-NUMBER>
    => Switched to branch and applied the changes.

Afterwards if I accepted the diff I can verify that my remote HEAD is the merged
diff. (WIP)

::

    $ git log origin master --oneline --short
    3f9e302 Super dope feature <AUTHOR-NAME>

And the diff is understood as accepted.

::

    $ rad diff list
    rejected   3   Commit message                   cloudhead     2019-01-25T13:27
    accepted   2   Super dope feature               juliendonck   2019-01-22T13:27
    accepted   1   New way of importing something   jkarni        2019-01-25T13:27

Questions
-----------

- How do we deal with names? -> Currently the git usernames are used.
- What happens to inline comments on updates (Improvement)
- as a collaborator, should there be a possibility to store all your repos you
  collaborate on to see all changes in one place. (Improvement)

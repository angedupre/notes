# Collaboration Flow Research

---

# Feature Definition

## What is it

Instead of just copying the functionality of existing centralized code hosting platforms we'd like to take a closer look and see if there are any high impact workflow improvements we can do.

## Initial target audience

We want to start focussing on [OSS maintainers](../oss-design-research/oss-research/roles-in-oss.md) since we see them as the users with the most pain points in the existing workflow. But also keep the [OSS contributor](../oss-design-research/oss-research/roles-in-oss.md) in mind, since they will be on the other side of this workflow.

## What problems do we solve?

We're trying to help relieve some of the feelings of being overwhelmed a lot of OSS maintainers have today. Specifically trying to improve the collaboration workflow around:

- Issue triage
- Proposal reviewing
- Commenting
- Roles & permissions in OSS repos
- Repository organization
- CLI interface

---

# Considerations

## Existing feedback

- [Roads and Bridges](https://www.fordfoundation.org/library/reports-and-studies/roads-and-bridges-the-unseen-labor-behind-our-digital-infrastructure/)
- Github
  - [Cloning vs forking](https://github.community/t5/Support-Protips/The-difference-between-forking-and-cloning-a-repository/ba-p/1372)
  - [dear-github issues](https://github.com/dear-github/dear-github/issues?q=is%3Aissue+is%3Aopen+sort%3Acomments-desc)
    - [Github Folders](https://github.com/dear-github/dear-github/issues/74)
    - [Discussion Tab](https://github.com/dear-github/dear-github/issues/44)
  - [isaacs/github](https://github.com/isaacs/github/issues?q=is%3Aissue+is%3Aopen+sort%3Areactions-%2B1-desc)
    - [Delete remove issues](https://github.com/isaacs/github/issues/253)
- [Rethinking Issue Management](https://gist.github.com/oelmekki/b9a89a7a524f7eac2414dfbe7fb2da89)
- SSB position on github
  - [Maintainer's role](https://viewer.scuttlebot.io/%25hEOaREi6NZJzJLYZn1WrKFJOWXS3CmwoR%2FMk6FRCrwM%3D.sha256)
- My research
  - [Overview of tasks](../oss-design-research/oss-research/common-tasks-maintainers.md)
  - [Roles in OSS](../oss-design-research/oss-research/roles-in-oss.md)
  - [Shadow Sessions Digest](../oss-design-research/shadow-session/digest.md)
  - [Alexis' doc](https://drive.google.com/a/monadic.xyz/open?id=11PG8j1FjQuvDudvTtHrgfPNLTF38io2BHRcHhgobPjE)

---

# Areas to explore

- cli
  - accessible issues & proposals
  - Entire workflow should be accessible through cli
- improving issues
  - [discussion?](https://github.com/dear-github/dear-github/issues/44)
  - rethinking notifications
  - allowing deleting of issues
  - Fast triage tools?
- Proposals
  - Improve review process
  - Who can review?
  - Make merging upstream commits easier to empower people to fork sooner?
- Proposals vs suggestions
  - Suggestions would be free floating patches that don't have to live in a pull request or a branch. They can be small things or big
  - How do we make this fit
- Repository organisation
  - [Folders?](https://github.com/dear-github/dear-github/issues/74)
  - follow folders
  - orgs?
  - Free floating repos?
  - Unix file system groups tags

---

# Research

### [I'm an open-source maintainer who doesn't always answer issues and pull-requests right away](https://news.ycombinator.com/item?id=5546166)

- You could always have the courtesy to acknowledge the bug or PR I've submitted.
  - maintainers can't just jump every time a contributor needs something done
  - how do we create the right expectations for the contributor
- They may get between 100 and 200 emails a day during the week.
  -      how do we improve the notification hell?
- it's often the sense of entitlement and lack of understanding that makes it enjoyable to respond to requests.
  - it's exhausting to the maintainer
  - how do we create an environment where contributors have an understanding for what it takes to maintain a project?
- "If you don't have time to maintain the project, then mark the project as not actively maintained so we can move on,"
  - Labeling the project as "unmaintained" would be short-changing all the people who are still actively using and developing and maintaining it.
  - sometimes a maintainer has a busy few weeks or months
  - how do we enable contributors to feel empowered to fork more quickly and maybe later easily merge the upstream changes or even just merge back into the original repo
- "But my change is really small, just merge it in,"
  - there is no such thing as a small patch
  - maintainer is responsible for everybody in the project, so can't risk small things to break the whole thing
- ...but I did and do think it's rude not to reply at all. "Thanks for the patch; don't know when I'll have time to look at it" is enough.
  - contributors would like to feel heard, and understand where the maintainers are at, even just to understand if the project is actively being maintained at the moment

### [What it feels like to be an open-source maintainer](https://nolanlawson.com/2017/03/05/what-it-feels-like-to-be-an-open-source-maintainer/)

- Types of issues:
  - badly formatted / bad english you try to decipher, give some general response, send some links
  - disgruntled user don't reply or say it's open source... + if there's a bug, submit reproducible
  - very common problem with easy workaround you google for a minute and reply with the solution + close issue
  - regular contributor has PR to solve esoteric issue you want to just merge it, but afraid that it might break some small things down the line will take you a lot of work to properly review, so you put it on the backburner
  - new bug, but is part of sibling project answer that it's related to this other repo and where they can start working on it
  - person asking what the status is of an older issue "Sorry, this issue has been open for a while, but nobody has tackled it yet. We're still trying to understand the scope of the problem; a pull request could be a good start!"
  - test bot restart tests and wait to see what happens
  - person opened PR other maintainer took a look at it, you glance, and move on
- "In a sense, these GitHub notifications are a constant stream of negativity about your projects."
- after a while go through all old issues and post "I'm closing old issues. Please reopen if this is still a problem for you or if you can provide more details." see what pops up
- After triaging enough issues like this, even if you eventually reach inbox zero, you might still end up with a large backlog of open bugs and pull requests.
  - how can we help triage & follow up
- Best thing to get more contributors & maintainers is to leave? To create a void for other so step up into

### [Trunk based development](https://trunkbaseddevelopment.com)

- Add some comments

### [How Gerrit works](https://gerrit-documentation.storage.googleapis.com/Documentation/2.15.3/intro-how-gerrit-works.html)

- Add some comments

### [Notes on Jane Street Code Review](https://blog.janestreet.com/putting-the-i-back-in-ide-towards-a-github-explorer)

- Sandboxed approach -> As soon as you add comments or edit the code (read > write) it makes a new snapshot on your machine and that is a new commit or history moment
- Entire workflow is available in editor -> emac / vim, no integration with vscode, ... so far
- "It feels like what an integrated development environment is supposed to feel like. Making software today is as much about collaboration as it is about writing your own code. But most developers are forced to switch from their editor to a web browser to read someone else's code, and switch back if they want to play with it themselves. Code review that takes place in a browser isn't just more inconvenient, it's often shallower, too: to really understand a piece of code you have to build it, run it, and explore it with your own hands, in your own editor. " -> ring true to what we talked about
- Feature explorer
  - call everything a "feature," but really they come in two flavors: features that are ready for review are the equivalent of pull requests, and features that you're just privately hacking away on are the equivalent of branches
  - when going into a feature, you see a "title page" and when you press enter you see a list of files with changes structured as a todo list
  - hit enter again and your in a diff view of all the changes in that file, you can just accept it and go to the next one or open it immediately in your editor in a sandboxed environment (all you need to do is commit, no switching branches etc etc)
  - you can leave notes as literal comments in the code that has a special but simple syntax

### [Notes on How Jane Street Does Code Review](https://www.youtube.com/watch?v=MUqvXHEjmus)

- Constraints:
  - All code has to be reviewed before it gets released > Including conflict resolutions!
  - You should never have to review something you've already reviewed.
  - You can always push new changes to a branch, regardless of the state of review.
  - You can rebase a branch at any time, regardless of the state of code review.
- Brains:
  - person-branch pair
  - empty diff called brain
  - as you review it changes
  - diff is applied to your brain
  - when you review something you brain remembers it (not the content)
  - you have to accept changes into your brain
  - as soon as you've reviewed everything that has changed in a branch, your brain equals the branch
  - if someone changes something upstream
    - you create a diff of your brain and the upstream change
    - a diff of a diff (of a diff)
    - only look at them if there are merge conflicts
  - cons
    - rebase force you to consider the diff of the entire branch > they make small branches
    - sometimes diffs of diffs are too complicated and you remove your brain and start over
  - advantages
    - you can always rebase, cause everybody has a brain and then they just have a new target to diff with
    - never have to read a commit twice
    - merge commits don't add complexity
- inline code comments
  - current state:
    - commenting on
      - diff
      - branch
      - current state of a file
  - when you comment inline it's always there
  - when you comment it shows up in the diff -> triggers your brain
  - where should comments go else?
    - commit can go away
    - on a diff is difficult with line changes
    - on a branch, but then have to reference lines which can change
  - they will disappear in the end when "merged"
  - pros
    - no context switch between addressing comments and replying to them
    - sometimes it's easier to fix then to point out problems
    - coding is more collaborative
      - your branch is not yours alone -> it will be public eventually
      - you "review" your branch just as your reviewer does
  - cons
    - messy history (can comment in separate commits and remove those when you "merge")
    - people got over the weird commit histories
- obligations
  - who needs to review
    - branch owners > polish
    - whole feature reviewers > read the whole thing and "second" it
    - file reviewers > permanent obligation that file stays lean and needs to be able to have an opinion
    - file owners >
  - files checked into version control
    - they declare metadata
      - owner
      - level of scrutiny > how many need to review it (have obligations)
      - per file / per directory
      - who needs to review
    - see screenshot
- nested branches
  - being able to branch of features (branches)
  - how it works
    - master
    - master/monad-transformers
    - master/monad-transformers/monadic-testing-dsl
    - master/monad-transformers/something-else
    - master/monad-transformers/something-else/deeper-nested
  - advantages
    - necessary to be able to do code review with brains
    - what you review is not a commit it's a branch
    - normally you make a branch and add multiple commits in order and you review them in order <> jane street each commit is a branch and you review them one by one
    - blurred lines between commits and branches
  - they have monorepo with master/app-name as subbranches > allows them to merge into the sub-master before releasing to the world
  - features instead of branches > branch + metadata (eg. owner)
- TODO
  - dashboard of what you're reviewing
    - what you're reviewing
    - the branches that you have
    - state of the branches (features)
  - overview
    - review
      - open cr's
      - responses
      - diff lines
      - next step
    - unclean workspaces
      - so you can clean up workspaces you might have forgotten
    - list of features that you own
      - hierarchical
      - shows nexts step
        - rebase
        - up to date
        - has crs
        - has changes
  - you can create a bunch of stuff and just go from one to another and this helps well, would be cool to contribute to a bunch of open source projects
  - you can rebase branches from the dashboard and will do it asynchronously
- Workspaces
  - you have these versions of checkouts not entire checkouts
  - you can just checkout
  - git worktrees
  - quickly switch between branches so you want to look at without having to shelve changes
  - deep nested directory of every branch you've ever looked at
  - different working directory per branch
    - switch to review branches has less of context switch
    - switching directories is much faster then switching branches
    - run multiple builds in parallel
    - no stashing
- locks
  - lock feature for release (cannot merge into parent)
  - lock rebase > difficult rebase you
  - won't let you release a branch that is not completely reviewed or has crs

### Hacker News articles

- [Why I close pull requests](https://news.ycombinator.com/item?id=13274064)
- [Code reviews and bad habits](https://news.ycombinator.com/item?id=7271445)
- [Pull request hack](http://felixge.de/2013/03/11/the-pull-request-hack.html)
  - [HN Discussion](https://news.ycombinator.com/item?id=5357417)
- [A plea for better open source etiquette](https://blog.quickpeople.co.uk/2013/04/14/a-plea-for-better-open-source-etiquette/)

---

# Workflow session

## Meeting notes Alexis & Julien 180719

- Issues:
  - Managing issues as a maintainer (especially with multiple projects)
  - Can we create an overview of all open issues in all your projects
  - One central place to manage all your OS projects
- Proposals
  - is there something we can do by disconnecting proposals from branches?
  - Can we enable people to do small contributions without having to always need a branch maybe "free-floating" patch sets
  - Think git squash approach
- Suggestions
  - in review process can we suggest code changes inline without having to make a new branch/commit/…
  - Suggestions can also function outside of review process
- How are proposals and suggestions similar and how are they different, do we need both?

---

# Contribution workflow

[See here](../../specs/ revision/collaboration-flow.md)

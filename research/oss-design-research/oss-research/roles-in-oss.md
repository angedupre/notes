# Roles in OSS:

## 1. Maintainer

### Description

Contributors who are responsible for driving the vision and managing the organizational aspects of the project. Maintainers are the most important actors within an open source project.

### Main responsibilities

- Authoring: author git commits on the git history
  - Converging commits: merge commits or that incorporate other branches/forks
  - Extending commits: extending the history of the codebase (every other commit)
- Request management: manage the backlog of requests
- Publishing & versioning: publish releases (distribution/naming/versioning)

[Overview of most common tasks](./common-tasks-maintainers.md)

### Problems

- No way to monetize their OSS work
- OSS work is the most important in their career but they can’t get paid for it: If you write code and keep it to yourself you have more chance of being able to make money off of it versus when you share it it's part of the public domain.
- It’s harder to accept contributions then to make them
- Lack of funding leads to frustration (My code is free, my time isn’t)
- Time management
- Hard to stay motivated after initial problem they set out to solve with the project is solved
- Very ingrateful job to be governing OSS projects, every users and contributor has their selfish reason to be there, governing is mostly about saying “no”
- Hard to find other maintainers/contributors to share the load with
- They are reluctant to start new OSS projects because of the work it entails
- Tools are catered to everybody, making them lack specificity for maintainers: Dear GitHub

### Success criteria

- Monetize
- Having recurring contributors
- Getting recognition
- OSS project doesn’t need them anymore

### Existing tools

- Version Control System (e.g. CVS, SVN, Mercurial, Fossil, Git)
- Bug & Issue tracker: Where people discuss issues related to the project.
  - Bugzilla/GitHub issues/Gitlab/Jira
- Archiving & release management (eg. [github-releases](https://github.com/aktau/github-release))
- Proposals: Where people discuss and review changes that are in progress.
- Discussion forums or mailing lists: channels for conversational topics others use the issue tracker for all conversations.
- Synchronous chat channel: Some projects use chat channels (such as Slack or IRC) for casual conversation, collaboration, and quick exchanges.
- Tools for funding (Patreon + opencollective/kickstarter)
- [Licenses](https://choosealicense.com/licenses/)

### User stories

- As a maintainer I want to have time to work on my OSS projects
- As a maintainer I want to get an income from my OSS projects
- As a maintainer I want recognition for the contributions I made
- As a maintainer I want my OSS to be hosted for free
- As a maintainer I don’t necessarily want to have to make all the decisions
- As a maintainer I want to have my OSS projects, OSS management tools and OSS projects’ community in the same place
- As a maintainer I want my workflow to change as little as possible

## 2. Contributor

### Description

Could be anyone who comments on an issue or pull request, people who add value to the project (whether it’s triaging issues, writing code, or organizing events), or anybody with a merged pull request (perhaps the narrowest definition of a contributor).

### Main responsibilities

- Authoring: author git commits on the git history
  - Extending commits: extending the history of the codebase (every other commit)
- Commenting & issue submission

### Problems

- Incomplete or confusing documentation
- Unresponsiveness of maintainers
- Dismissive responses, leading to contributors leaving
- Conflict through bad communication
- Unexplained rejection making contributors feeling like they wasted their time
- Proposals not being accepted leading to contributors moving on

### Success criteria

- Merged contribution
- Getting recognition
- Original bug/problem is solved

### Existing tools

- Version Control System (e.g. CVS, SVN, Mercurial, Fossil, Git)
  - Bug & Issue tracker: Where people discuss issues related to the project.
- Bugzilla/GitHub issues/Gitlab/Jira
- Proposals: Where people discuss and review changes that are in progress.
- Discussion forums or mailing lists: channels for conversational topics others use the issue tracker for all conversations.
- Synchronous chat channel: Some projects use chat channels (such as Slack or IRC) for casual conversation, collaboration, and quick exchanges.

### User stories

- As a contributor I want to have a clear path to contribute to a OSS project
- As a contributor I want to feel that my contributions matter
- As a contributor I want to see a OSS project is being maintained
- As a contributor I want one accessible & searchable place to see all the most relevant OSS projects

## 3. User

### Description

People who use the project. They might be active in conversations or express their opinion on the project’s direction.

### Main responsibilities

- Use project
- Report bugs

### Problems

- People rely on OSS that is not actually maintained properly or doesn’t have a robust built
- Incomplete or confusing documentation
- Unmaintained project (unmaintained dependency)

### Success criteria

- Bugs get resolved quickly & often
- Project is continuously maintained
- Accessible and understandable licensing

### Existing tools

- Version Control System (e.g. CVS, SVN, Mercurial, Fossil, Git)
  - Bug & Issue tracker: Where people discuss issues related to the project.
- Bugzilla/GitHub issues/Gitlab/Jira
- Discussion forums or mailing lists: channels for conversational topics others use the issue tracker for all conversations.
- Synchronous chat channel: Some projects use chat channels (such as Slack or IRC) for casual conversation, collaboration, and quick exchanges.
- Source code scanning and license compliance (more corporate)

### User stories

- As a user I want to find projects that solve my problem so i don’t have to build everything myself
- As a user I want to see that an OSS project is being maintained so that I know that it’s a “good” project
- As a user I want my questions to be answered quickly so I can continue the work this is depending on
- As a user I want clear documentation so I can quickly see if a project will solve the problem I’m looking to solve
- As a user I want the maintainers of the project to be responsive to my problems
- As a user I want the OSS project to have accessible licensing so I’m able to use it at my place of work

## Sources

- From the [Oscoin user story document](https://docs.google.com/document/d/1nyqT5YkOWVXsx-5R8EG8iUZ53_N7eeiuazOYXtM7PdM/edit?usp=sharing):
  - Maintainers: Maintainers are the most important actors within an open source project. They code, they answer issues, they review and merge contributions and keep the community together. They are our main target audience. If we succeed in satisfying their needs, we will succeed everywhere.
  - Contributors: Somebody who has contributed code through patches & proposals
  - Users / Companies: A company or an individual just want to use an open source package
  - Token Holders:
- Validators / Hosters: Validators are rational actors. They want to maximize their profits. It’s helpful to think of them as rational animals, despite the fact that some of them might have additional incentives.

- From [here](https://opensource.guide/how-to-contribute/#anatomy-of-an-open-source-project)
  For some projects, “maintainers” are the only people in a project with commit access. In other projects, they’re simply the people who are listed in the README as maintainers.

  A maintainer doesn’t necessarily have to be someone who writes code for your project. It could be someone who’s done a lot of work evangelizing your project, or written documentation that made the project more accessible to others. Regardless of what they do day-to-day, a maintainer is probably someone who feels responsibility over the direction of the project and is committed to improving it.

  A “contributor” could be anyone who comments on an issue or pull request, people who add value to the project (whether it’s triaging issues, writing code, or organizing events), or anybody with a merged pull request (perhaps the narrowest definition of a contributor).

  The term “committer” might be used to distinguish commit access, which is a specific type of responsibility, from other forms of contribution.

- Github Roles:

  - Author: The person/s or organization that created the project
  - Owner: The person/s who has administrative ownership over the organization or repository (not always the same as the original author)
  - Maintainers: Contributors who are responsible for driving the vision and managing the organizational aspects of the project. (They may also be authors or owners of the project.)
  - Contributors: Everyone who has contributed something back to the project.
  - Community Members (users): People who use the project. They might be active in conversations or express their opinion on the project’s direction.

- Roles based on [this article](https://viewer.scuttlebot.io/%25HPMQEUbULKcJJMEAP%2FiMnVfuykNZ9llEymArjkuEO%2FA%3D.sha256)
  Conclusion: in a free cyberspace, the social dynamics of open source collaboration would be voluntary with ephemeral roles, not permanent titles
  Roles: git Extenders, git Convergers, Reporters, Community gardening, Distributors, Namers (Onomatologists), and Contract Compatibility Analysts.

  Maintainer Roles:

  1. Authoring: author git commits on the git history

  - writing git commits
  - two types of commits:
    - convergence: merge commits or that incorporate other branches/forks
    - extension: every other commit -> extending the history of the codebase (not necessarily a divergence)

  2. Request management: manage the backlog of requests

  - Bug reports, issues, pull requests are sent to an inbox
  - The inbox is a community

  3. Publishing & versioning: publish releases

  - Maintainer needs to npm publish (or equivalent)
  - Three responsibilities
    - distribution
    - naming
    - Versioning

  Contributors:

  - Employed developers: People at companies submitting pull requests - Mostly there to solve their own problem and move on
  - Weekend Devs: might fix some bugs - limited amount of time
  - Students: Take more effort to maintain their contributions, because they have lower level of knowledge, but if treated well have the highest potential to become longer term contributor/maintainer.

  Users: They use the OSS and might be commenting on some issues and proposals or asking some questions

  - Potentially low cost to maintainer, but depends on size of project, can become very noisy

  (Ab)users: ask you to add something to the project and only then would they use your project

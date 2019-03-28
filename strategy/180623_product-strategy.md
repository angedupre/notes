# Product Strategy

## Goal

We want to create a world where OSS participants can gain independence from classic wage-slavery. Where OSS is valued by the companies who depend on it and that trickles down to the maintainers and contributor in the form of rewards, ownership & recognition. OSS projects, but possibly all products, will be able to break free from the existing arbitrary structures of collaboration through programmable governance systems and those will be part of what these projects contribute to the OS world.

At the same time, it's important to us that we don't create a gig economy where developers get abused, that we keep organizations from centralizing too much power and keep people from trying to abuse the commons in order to enrich themselves.

## Phases

-- MVP --

1.  Improve and facilitate collaboration on top of oscoin protocol (compete & improve)

2.  Bring in incentivization with the token (differentiate)

-- POST MVP --

3.  Developers gain independence from classic wage-slavery (adoption)

## Platforms

- collaboration & incentivization toolkit
  - Web interface
  - CLI interface
- SDK \*
  - Radicle \*

## Target Audience

Phase 1:

- Developers: Maintainers, contributors, users, core developers, …
  - add example projects \*

Phase 2:

- Network Operators: Validators, ...
- Service Providers: Exchanges, wallets, ...
- Token Holders: Investors, speculators, OSS funds

---

## MVP phase 1: Improve and facilitate collaboration

**Framework**

- \_A showstopper: \_People won't buy your product if you're missing this feature, but adding it won't generate demand.
- _A game changer:_ People will want to buy your product because of this feature.
- _A distraction:_ This feature will make no measurable impact on adoption of the phase we're in.
- _Freezer:_ Post MVP features

### 1. Showstoppers

- Support existing git features
  - Repository View
    - readme
    - file browser
    - source viewer
  - Commits
    - Log
    - diff view
  - Branch
    - merging flow
    - diff view
  - Authors
    - permissions
- Users
  - Log in / keys
  - Account
- issues
  - Creating issues
  - closing issues
- proposals
  - creating proposals
  - merging proposals

### 2. Gamechangers

- [workflow improvements](../research/code-collaboration-research/collaboration-flow-research.md) > Define "our" code review workflow
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
  - Repository organisation
    - [Folders?](https://github.com/dear-github/dear-github/issues/74)
    - follow folders
    - orgs?
    - Free floating repos?
- admin through aggregate signatures
  - collective decision making
- Extensibility of the protocol
  - make Radicle accessible to "everybody"
- leveraging decentralised approach
  - Offline accessible

### 3. Distractions

- private repos \*
- visualizing impact independant of contribution graphs
  - Following (repos, people, dependencies, orgs)
- enterprise

### 4. Freezer (things that we build post MVP)

- explore
  - eg. tree structure to see what is the most relevant fork
- CI/CD
- Programmable administration

- to be reviewed

---

## Approach

We want to start by focussing on the "gamechangers", building out the "showstoppers" along the way. Starting with the workflow improvements, which you can follow that process [here](https://docs.google.com/document/d/1l5GShxEFZ7yYqPgUhSA2lJiDfbtIOLMs1QqBxBLZIIU/edit?usp=sharing).

Basically we're going to map out the entire user journey both for the Maintainer and the Contributor, trying to identify pain points along those journeys. We then want to use those to create an improved workflow, resulting in our own code review approach (eg [Github Flow](https://guides.github.com/introduction/flow/)) with a GUI and CLI to interface with it.

---

## Sources

- [Workshop Digest](../../workshops/180706/product-discovery-digest.md)
- [dear-github issues](https://github.com/dear-github/dear-github/issues?q=is%3Aissue+is%3Aopen+sort%3Acomments-desc)
- [isaacs/github](https://github.com/isaacs/github/issues?q=is%3Aissue+is%3Aopen+sort%3Areactions-%2B1-desc)

# Radicle.xyz

## Roles & Responsibilities

- Release scope [Alex]
- Brand [Sam & Roon]
- Content Strategy [Julien & Sam]
- Copywriting [Sam]
- Information Architecture [Julien]

---

## Content strategy

### Why

_Know the business case and objectives. Why are you embarking on this project?_

We'd like to introduce the radicle vision, of a P2P open source collaboration network, to a wide audience. Since we want to get an MVP out sooner rather then later we're looking to make a limited feature available that highlights a very basic collaboration flow. From there we can get people excited about the project and begin an open source working process so users can give us feedback or participate on the codebase.


### What

_What is the message?_

If my team wants to make software together why do we need a third party to manage the relationship? Sharing code peer-to-peer is intuitively how I want to collaborate on code.

OSS development is inherently P2P. Radicle encodes this relationship into the protocol, making the collaborative process itself programmable.


### Who

_Who is the audience?_

1. People that are interested in decentralized ways of organizing and gorwin a P2P ecosystem

  - This group is disaffected by the extractive practices of tech monopolies Google, Amazon, Facebook, and Apple -- many are also skeptical of the capitalist model that gave rise to these organizations. They may have a sense of nostalgia for the early web era that seemed simpler and less politically fraught. Members of this group are often more idealistic and more artsy than the typical programmer, they value the importance of trustful (as opposed to trustless) relationships. We would like to develop a tone of voice that is friendly, welcoming & honest that speaks to this group.
  - Ande Saltz discussing P2P github alternative: %VMSPdm6JIdHvi3Bl0iZi+P+qB66OlTsnfy7pl4mmPhI=.sha256
  - noffle discussing scalability issues with git-ssb: %eNzWradArYP6BUtmz+6HgG0S+XkwDPXstAQ4/OuE+0w=.sha256 , %eNzWradArYP6BUtmz+6HgG0S+XkwDPXstAQ4/OuE+0w=.sha256
  - bobhaugen discussing with mastodon community GitHub alternatives: %r/6bLB3kimrlHqOUKAgHqXFyrVLW90xLM0/9j6FsM1s=.sha256

2. DWeb technologists (mozilla / brave / blockchain developers)

    - This group is interested in experimenting with new technologies to see how the dweb ecosystem fits together as a whole. They are interested in development but perhaps more closely attuned to the technical/architectural choices in order to evaluate whether they should invest further into the technology and better understand how the tech might eventually connect to their own technical infrastruture.

3. Functional programming / Lisp enthusiasts

  - clojure/lisp/scheme developers
    - they should already be familiar with the programming paradigm, so maybe radicle is something they can pick up quickly and hack together a cool demo
    - want to evaluate whether radicle might be somthing that plays well with a unified lisp development environment

  - haskell & academic developers
    - might browse radicle's source code because it's a significant project that was built with haskell
    - people who might be interested in reflective towers & other design choices within the language itself
    - _This cohort probably won't be addressed until we make the REPL documentation available_

4. People that are interested in open source & code collaboration

  - Those who are looking for flexibility in tooling - they've heavily customized their computing environment, window manager, .profile files, maybe written their own emacs or vim plugins. Perhaps they'd also like to extend this flexibility to their revision control platform, see the following:
    - dear-github/dear-github#44
    - dear-github/dear-github#74
    - https://news.ycombinator.com/item?id=5357417
  - Those who are interested in an open source approach, they've published their own tooling on github or gitlab, even if they're package isn't wide use, they're committed to the idea of openly publishing the code for they produce for personal projects
  - Those who are looking for an alternative to github, *not* those who want a feature complete alternative (Gitlab/...) - perhaps they moved from GitHub to GitLab or another platform after the Microsoft aquisition, or seriously considered doing so, but haven't found the right service to commit to.


### Where

_Where will the message be read (location, device, context)?_

- Twitter / Mastodon
- Community newsletter
- IRC
- Scuttlebutt
- Reddit / Hacker News / lobste.rs
- Are.na / Pinboard

- Social Networks
  - [Scuttlebutt](https://www.scuttlebutt.nz/)
  - [Fediverse](https://fediverse.party/en/fediverse/)
  - [Matrix](https://matrix.org/blog/home/) - kind of like decentralized slack that interops with IRC, XMPP, etc


### How

_How should we present/structure the content?_

Since we want to focus this release around the collaboration piece, I think we can work with a subdomain of radicle.xyz. Something in the form of radicle.xyz/code-collaboration, where we can focus the communication on highlighting the code collaboration flow & experience. From there the user should be able to navigate to the radicle.xyz homepage where they can find more information about the radicle stack, containing the language & replication layers.


### When

_Timing of the process to create and publish the content._

First week of February 2019


## Information Architecture

See a live demo here of what Julien had in mind: http://reflective-toy.surge.sh

The structure below is similar, Sam reshuffled some of the items and added a few things.

- Radicle.xyz
  - Home
    - Introduce radicle stack
      - What is the radicle stack? -> P2P collaborative programming language
      - What is it for? -> writing collaborative programs whose shared history helps teams coordinate and create together
      - Why collaborate with radicle?
    - Get started
      - How to install
      - Link to collaboration suite (PRs, issues) tutorial (e.g [try-dat](https://try-dat.com/03-modify.html))
  - Docs
    - Radicle collaboration apps
      - Guide - walks through typical collaboration flows with radicle
      - Reference - searchable index of all commands and flags, including descriptions and examples
    - Radicle language
      - Specification (white paper)
      - Guide (current housed [here](http://docs.radicle.xyz))
      - Reference - searchable index of functions and other objects, including descriptions and examples
  - Blog
    - Intro post (move from oscoin.io)
    - Community values
    - Future of the radicle stack
  - Source Code
    - Radicle codebase
    - Radicle issues app
    - Radicle pull requests app
  - Chat
    - Live in-browser gateway to our IRC chat. Pick a user name and ask the team a question. https://github.com/kiwiirc/webircgateway
  - Colophon (footer)
    - Using X open source blog platform
    - Contributors list
    - Open source typeface
    - Hosted on IPFS & Dat - website needs to consist of static assets to acheive this

---

## Examples

- Design vibes

  - Home page & radicle guides experiences that read as a fluent story
    - Roon's work Julien liked: [googlefonts.github.io/korean/](https://googlefonts.github.io/korean/)
    - Interest level & play: [keen on](http://codes-algorithms.keenonmag.com/editorial/)
    - Interactivity level: [reactjs.org](https://reactjs.org)
    - Content pacing & playfullness: [Handmade Computer](http://avant.org/project/zero-one/) of an article that I edited that takes Korean online scroll comics as inspiration
    - Content pacing & tone: [gt-america.com](https://gt-america.com)
    - Interest & play: [what is code](https://www.bloomberg.com/graphics/2015-paul-ford-what-is-code/) elaborate scroll
    - Clarity of visual explanations: [nice interactive scroll](http://www.r2d3.us/visual-intro-to-machine-learning-part-1/) intro to machine learning
    - Balance between playfulness and explanatory: [notion.so](https://www.notion.so/product)
    - Playful and well-paced: [2019.cssconf.eu](https://2019.cssconf.eu)

  - Language guides & reference documentation
    - [reactjs.org](https://reactjs.org)
      - informative landing page
      - intuitive navigation
      - comprehensive & structured
      - interactive examples
    - [ponylang.io](https://www.ponylang.io/)
      - Questions and in navigation, super easy to find stuff
      - Navigation targets audience
      - Very concise and clutter free
      - Tutorial appearance differs and repeats stuff from the homepage website :(
      - No code example on the home page :(
    - [purescript.org](http://www.purescript.org/)
      - Homepage fits on a screen!
      - Two main CTAs “Quickstart Guide” and “Try Purescript” don’t clearly differntiate :(
      - Clearly visible tagline
    - [elm-lang.org](https://elm-lang.org/)
      - Wording is a bit off. “Install” should be “Get started“, “Feature” sounds to dry
      - Sparse, but I’m not missing any information
      - first action install
      - approachable overview of the feature set
      - compelling examples
      - digestable docs
    - [d3js.org](https://d3js.org/)
      - strong visual hook
      - fast actionable tutorial
    - [clojure.org](https://clojure.org/)
      - Tagline with prominent “Get started” CTA
      - Text blob by creator above the fold that nobody reads
      - No code snippet
    - [racket-lang.org](https://racket-lang.org/)
      - "Technical" feel
      - Links to all the stuff I am looking for.
      - Amazing docs.
    - [reasonml.github.io](https://reasonml.github.io/)
      - Very clear, good nav.
      - Good docs.

- Other ideas / references:

  - [grx-inno](https://amiga.textmod.es/colly/grx-inno/)
    - good ASCII scroller
  - [glitch.com](https://glitch.com/)
    - web-based collaborative coding that's inviting
  - [delinear.info](http://delinear.info)
    - exploratory & weird
  - [stimuleringsfonds](https://www.talent.stimuleringsfonds.nl/2015/)
    - nice use of parentheses
  - [datproject.org](https://datproject.org)
    - intuitive navigation
    - good guide [try-dat.com](https://try-dat.com/)
    - to the point communication
    - mediocre design
  - [Scuttlebutt Protocol Guide](https://ssbc.github.io/scuttlebutt-protocol-guide/) / [Dat Protocol Guide](https://vtduncan.github.io/how-dat-works/)
    - nice balance between comprehensibility & detail
  - [Beaker Browser](https://beakerbrowser.com/docs/tour/)
    - walk-through is often cited as very approachable
  - [RenkArt](https://renkonline.org/#/about)
    - nice use of text
  - [cameronsworld](https://www.cameronsworld.net/)
    - weird web 1.0

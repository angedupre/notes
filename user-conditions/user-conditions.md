Radicle User Conditions
=======================

This document outlines a set of user conditions that we should have in mind when developing products within the Radicle ecosystem. Initially, these conditions aim to be representative of target users for the Radicle Alpha Release.

All descriptions are given in the first person from the perspective of a proto-persona / radicle user.

The conditions are split into several themes, each with a textual description and related user stories. These user stories are meant to operate at a higher leve of abstraction than the current *UX Flows* specifications. As these user stories solidify, they may get migrated to their own documents or be used as a promt for future UX Flows / product specifications as well.

## Code Collaboration Context

Github pretty much is my social network. I’m excited about the idea of moving some of my coding project to a P2P environment, especially after the Microsoft / Github acquisition. It seems politically aligned with my desires to delete my facebook account and use less centralized platforms. However, I have a hard time imagining a p2p tool covering all of the use cases and social aspects of a project like github.

From a more pragmatic/usability standpoing, I'm excited about the programmability and configurability of code collaboration workflows. I like the idea of a project's community deciding on what kind of collaboration tools they use, and these tools all being open source, similar to the open source plugin ecosystems around code editors, but for collaboration apps.

Initially, I came across Radicle as an individual, excited by the mission describe on radicle.xyz. I have a few friends who I collaborate with on some code projects that I think might be interested in the project as well, but first I want to explore Radicle by myself and test out its functionality before i ask friends to collaborate with it.

To test out the code hosting tools, I’d like to take an existing repo I have, and try porting it to Radicle. However, to to try out the cool "code collaboration tools" described on the radicle.xyz website, I need to find some existing content that I’d like to collaborate with.

I want to find out if projects that I am interested in are hosted on radicle. At a later stage, I’d hope to be able to see on a projects github page that they accept issues/PR’s via Radicle, but for now, I would expect that somewhere on Radicle I can see an index of interesting projects that are experimenting with Radicle as a tool for code hosting & collaboration.

After testing out collaboration on some highlighted projects, I’d like to invite some friends to collaborate with me on radicle. I do that by pointing them to the radicle.xyz site, and giving them the necessary details (e.g. repo  identifier) of how to find my project on the radicle network.

### Related User Stories
- I want a clear path to discover and explore projects that are already hosted on radicle so I can test out Radicle for code collaboration
- I want to understand the code collaboration framework of radicle, and how its different from github (PRs, forking, merging)
- I want to be able to contribute to someone’s project, and not necessarily “fork” the repository (github style)
- I want to get notifications of new information from my Radicle network (project updates, diffs accepted, issues commented on…)
- I want to be able to see a list of projects or users that I've interacted with
- I want know (and potentially be notified) when project's i'm interested in are updated
- I want to be able to easily see what radicle projects I am following/seeding
- I want to have the ability to follow somebody's activity on the Radicle network so I can collaborate with people I already know on new projects of theirs
- When following a repo, I want to know who is the maintainer of that specific fork / repo instance that I’m following

## Identity Context

Because I’ve dabbled in some crytpo/p2p projects before, I am comfortable with using hashes / public keys as identifiers for content & users. It’s fine if there aren’t human readable names as primary identifiers, but any human readable metadata that I can get from a project (similar to a scuttlebutt user’s about section, or subjective “aliases”) will make interacting with repos on Radicle more comfortable for me.

Since I have a generally altruistic outlook on the developer ecosystem and people’s intentions in p2p communities, I trust that repos I see on radicle are being hosted honestly, and by the maintainers of those projects. If I have reasons to question the this, I’d probably see if I can find a link to this radicle repo ID somewhere on that maintainer’s other sites that I know and trust (personal website, twitter, scuttlebutt feed, github repo).

### Related User Stories
- I want to know that other users are who they say they are
- When following a repo, I want to know if that repo claims to be a canonical fork (main source of truth)
  - What package managers / distributions does this fork push to?
  - What are the uses of this instance of the given repo?

## Programming Experience Context

My first language was javascript, and though I still consider it the language I’m most comfortable in, I’ve spent the past 2-3 years exploring other programming languages like Rust or Go. I’ve heard of Haskell (read [a few blog posts even](http://adit.io/posts/2013-04-17-functors,_applicatives,_and_monads_in_pictures.html)), and get that it has quite a strong functional programming language community. Most of my understanding of functional programming comes from reading about [differences between React/Redux and Cycle.js](https://staltz.com/some-problems-with-react-redux.html).

I'm comfortable in the terminal, using basic unix commands and such. I'm enticed by the idea of having collaboration tools in my terminal, but my UX expectations are quite high since I'm used to using tools like github instead with a well designed web UI.

As for crypto, I’m definitely interested in the space and aware of the high level concepts like PoW, PoS, zk-snarks, etc. However, when it comes to implementing or interacting with this tech, I’d better hope that there’s a good Medium tutorial to help walk me through an implementation.

Peer-to-peer space still feels new to me. While I have a comfortable understanding of what things like DHTs are, if I had to debug a system that involved one, I would find it pretty difficult. Give me an easy way to run software, and a sandboxed way to experiment with my own applications / configurations, and I’m good to go!


### Related User Stories
- I want to be able to download and interact with radicle-stack/radicle-lang without having to build anything from source
- If I have problems getting radicle running, there should be a way for me to report issues without being able to submit to the “rad issues” RSM (email / irc?)
- I want to be able to build software & web-based apps in my language of choice that interact with radicle

## Data Availability / Synchronization Context

I expect most p2p software to work similarly to bittorrent’s “seeding” or dat’s concept of “peers” on their p2p websites. It makes sense that I should be mindful of having enough peers seeding or replicating my Radicle projects incase I go offline.

If there’s an easy way to pin or seed my radicle RSM’s on a server, I might explore that idea, but would need a pretty easy way to install or bootstrap that. Ultimately, it shouldn’t be harder than something like [hashbase](http://hashbase.io), and it should go without saying that I’d rather not give up any control or private keys to a server that replicates my data :)

### Related User Stories
- I want to consistently be able to resolve the latest data from an RSM identifier
- I want to know whether my updates will be available to the network when I go offline
- I want to be able to configure whether my computer actively or passively synchronizes repos that i’m subscribed to, so that I don’t start downloading software onto my machine without me knowing
- I want to know when I have stale data for a given radicle project or RSM

## Code Collaboration

Radicle.xyz Docs
=========================


This document outlines initial structure of the radicle.xyz docs page, which will be generated from a set of markdown files (per section).



+ Introduction [Cory + Sam]

  - The case for Radicle
  - Terminal first, offline first
  - Radicle & OSCoin (maybe?)

+ Installation [Hold, until packaging]

  - OSX
  - Linux
  - Build from source
  - Background processes

+ Get Started [Sam / Julien] (maybe better title)

  - Contribute to a project
  - Start your own project

+ Terminology & Key Concepts [thomas]

  - Radicle State Machines (RSM)
  - Radicle language
  - Radicle daemon
  - Radicle apps
  - Radicle projects
  - Storage & Networking in Radicle / radicle-p2p (this can be a teaser that leads into rad-p2p architecture section)

+ ``rad`` CLI Reference [merle / julian]

  - ``rad issue`` commands [julian]
  - ``rad diff`` commands [merle]
  - ``rad project`` commands [julian]
  - ``rad key`` commands [merle]


+ Background processes [Hold, until packaging]

  - OS X (brew services)
  - linux (systemd)
  - manual

  - radicle daemon
  - ipfs daemon

    * how do i check if they're running
    * how do i start them
    * how do i debug them
    * why do I need them

+ Radicle-p2p Architecture [julian]

  - How replication works
  - writing to an RSM (``ipfs-pubsub``)
  - the radicle language & how apps are written
  - how querying works
  - the radicle daemon / how relaying works

+ git repository hosting/storage [kim ?]

  - preamble (you can use any git repo with radicle...)
  - github/gitlab
  - decentralized (``git-ipfs``)
    
    * due to the way ipfs works, you need to make sure somone else reads the thing you pushed, or you need to stay online

+ Limitations & Troubleshooting [julian]

  - Installation Troubleshooting [whoever does packaging]
  - IPNS lifetime
  - Networking Issues (firewall, nat traversal)
  - Replication & Availability (cannot resolve RSMs)
  - ``git-ipfs`` limitations [kim]

+ FAQ

  - Why is P2P important for code collaboration?
  - What is the trust model of Radicle?
  - What is the difference between Radicle and Github / Gitlab ?
  - What is the difference between Radicle and other P2P projects like Dat or Scuttlebutt?
  - What is the relationship between Radicle and OSCoin?
  - Why is Radicle built on IPFS? [thomas]

# user research digest

## Action items

- Radicle work
  - [ ] `rad diff` to `rad patch`
- Website work
  - Front page
    - [ ] in 3 value props
      - [ ] P2P: make copy more concrete
      - [ ] Terminal first: be explicit that projects contain repo + issue + patch in cli
      - [ ] programmable: something like "ever dream of creating your own issues app..."
    - [ ] apps -> utilities
      - [ ] make asciinema > static + highlight some functionality
      - [ ] setup a project: mention issues patches repo
      - [ ] manage your issues: more to the point, call it "radicle issues" to decouple from GH??
      - [ ] collabor... > "propose changes": mention that they are like super basic PR's?
    - [ ] Stack / Architecture section:
      - [ ] focus on giving a mental model of what is going on
      - [ ] illustration update + clean up
      - [ ] link should go to architecture section
    - [ ] footer: think of issues being there before mentioning it
  - docs
    - [ ] intro
      - [ ] case for radicle > FAQ
      - [ ] get involved > own section in bottom of docs
      - [ ] new section: WHAT IS RADICLE
    - [ ] Installation
      - [ ] mention manually running the daemon in OSX and Debian sections
    - [ ] Guide
      - [ ] around `rad diff propose HEAD` section
        - [ ] HEAD > hash
        - [ ] explain where author comes from
        - [ ] single commit only disclaimer
        - [ ] commit message fix
  - visual
    - [ ] fix image
    - [ ] redo illustration
    - [ ] style 404
    - [ ] remove asciinema
  - Language ambiguity
    - [ ] diff, patches, proposals, ...
    - [ ] tutorial 1: commands should be code blocks in intro
    - [ ] Doesn't know what a **proposal chain** is
    - [ ] wording around proposals/diffs/patches is used in different places.
    - [ ] in tutorial part 2 intro: "..., however..." is confusing

## Individual **sessions**

### Debrief meeting

- Top level value prop is unclear
- Top level overview of “what radicle is” is unclear
  - “A Radicle project contains a git repository as well as the all the issues and proposals associated with that repo.”
  - Radicle “apps” is confusing
    - Utilities, tools, plugins
  - May benefit from elevating “project” and making that the main explanation of what radicle is
- Unclear about when doing an action actually has an impact on other peers
  - “Rad diff propose 0” … Did that actually send to someone?
- Could benefit from a “Radicle for GitHub users”
  - Radicle does git stuff for you
  - How does this change from your existing experience?
- The stack illustration is unclear
- “Rad checkout” should be more transparent about what files it puts where - transparency is key
- Radicle github needs to be up to date, and aligned with teh website messages
- delay between locally created issues and seeing it when it lists is jarring

### Billy

- Missing solid one line explaining what it is
- Confusing terminology:
  - apps vs utilities
  - diff, patches, proposals, ...
- Terminals are too fast and confusing
  - restart button
  - step by step approach
- Stack section is confusing + illustration confusing
- Installing
  - would like more transparency around running the daemons (in the background etc)
  - would like to get confirmation when installed e.g.: type `rad --help` to see if installed
- Guide
  - AHA MOMENT: "A Radicle project contains a git repository as well as the all the issues and proposals associated with that repo."
  - `rad diff propose HEAD` thought he was pushing his branch to the repo
- suggests a brief overview of the rad commands compared to git/github commands

### Sarah

- She often expressed that she only skimming through pages to get a general feel but did not read the details. This meant she missed a lot of information.
- Decentralised Github is not big enough selling point to seriously start using it.
- Used a lot of copy/paste of code from the docs.
- She spend a lot of time inspecting the readme on Github.
- She was confused about the messaging. From the website whe got “decentralised Github” but from the readme “programming environment”.
- She wants to know what commands do, which files they create before running them.
- Was very intrigued by the nature metaphor, especially the garden.
- She skipped the issues part of of the tutorial and was not interested in the second part (though we ran out of time).
- She only looked at the “Tutorial Part 1” and “Install” sections from the docs

### John

- rad daemon was run with "&" and output came into terminal window, which was confusing
- ran into double commit issue, proposal was rejected, second commit made and then ran into issues with second proposal, assumed system was broken
- didn't understand where data was being stored and sent
- "what is the radicle network?" how do we interact with it?
- initially thought project == repo
- diff vs PR isn't clear
- why use this vs normal git isn't clear
- moved his git projects on a rasberry pi and collaborates through that

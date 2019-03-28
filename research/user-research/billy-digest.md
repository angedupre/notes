# Main feedback

## Key takeaways

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

## Language fix

- tutorial 1: commands should be code blocks in intro
- Doesn't know what a **proposal chain** is
- wording around proposals/diffs/patches is used in different places.
- in tutorial part 2 intro: "..., however..." is confusing

## general feedback

- decentralization
  - decentralized things are good, open to experimenting with it, understands it's important in a general way of things
  - is often surprised that there are certain perks that come with decentralized tech
  - his attitude towards decentralisation: make github harder but decentralized (benefit in that long run)

## Feature request

- following orgs:
		- github doesn't let you subscribe to orgs on github,
		- would love to do that, social aspect is important to him, collaboration is important

## Log

### Header section

- didn't like image
- was confused by the language
- lots of text, little that actually communicates what it is, is missing a solid one liner
- the use of the word "apps" is confusing, could be utilities

### App section

- likes that it's a wrapper around git
- finds the asciinema confusing
  - should be short and simple. Maybe static?
  - maybe restart-button
  - Would be great to be able to control the terminal commands, click trough or something
- not super into the CLI

### Stack section

- word "syncs" makes him think he can make changes, wonders if git allows that as well
- knows patching terminology from github and gitlab, doesn't know particularly here what it alludes to
- what's the difference between maintainer and project owner
- is alpha a project release or part in radicle
- Illustration
  - is it a diagram from decentralized to centralized
  - sees it as ecosystem map
  - would you still interact with gitlab and github
    - are they related to how he's working

### Docs

#### Installing

- is confused by the 'launchd' word
- doesn't want the daemons to to run all the time in the background
  - is unclear that he can launch them as a temporary daemon
  - would like it to be clear that they can run the daemons in the foreground as well
- would like to be prompted to run `rad --help` to know if the brew install succeeded
- takes a look at the `rad keys` file to see if there's any kind of identity connected to it. Thinks identity is important for any social interactions.

#### Guide

- AHA MOMENT: A Radicle project contains a git repository as well as the all the issues and proposals associated with that repo.
- Confused if he needs to create a folder before checking out the project.
  - wonders if it the same as a clone or not
- `rad diff propose HEAD` might be bad wording, since it doesn't explain you should add the commit hash and is not clear to everybody.
- thinks when they are proposing a diff, they are pushing a branch to master. Is confused by the diff terminology
  - suggests a brief overview of the rad commands compared to git/github commands

## rough notes:

- doesn't know what code collaboration means
- is this related to peer-to-peer reminds him of a different group that has similar
- image is gross, kind of looks like penis
- reads through three titles
	- doesn't understand conversations through code
	- understands that issue and diff to terminal like github
	- find the sections confusing
	- too much at once
	- decentralised / peer to peer and ipfs stand out skims through it, theres a lot going on
	- theres a lot of text that repeats itself but
	- git like tool in the terminal, might be obvious cause he knows what we're doing
	- making apps: code collaboration makes him think of vscode code collaboration and google docs
- apps section
	- wrapper around git, thats cool using existing git repos
	- terminal is too fast to read everything (might need a restart button)
	- typo
	- doesn't necessarily want to use github in the cli
	- terminal goes to quick and there's too much going on SIMPLIFY
	- Not into cli
	- ipfs -> decentralized things are good, open to experimenting with it, understands it's important in a general way of things
		- would try because it's decentralized
		- is often surprised that there are certain perks that come with decentralized tech
	- git already gives him the tools to collaborate on code
	- tracking projects are more important to him
		- github doesn't let you subscribe to orgs on github,
		- would love to do that, social aspect is important to him, collaboration is important
	- ATTITUDE: make github harder but decentralized (benefit in that long run)
	- Would be great to be able to control the terminal commands, click trough or something
	- likes globe
- Would spend time on company content cause we send sparse content out
- stack section
	- syncs makes him think that they can make changes to it, doesn't git do it aswell
	- not sure what sync stands for
	- is unsure of the git that the maintainer flow works on git in general
	- knows patching terminology from github and gitlab, doesn't know particularly here what it alludes to
	- what's the difference between maintainer and project owner
	- is alpha a project release or part in radicle
	- looks at illustration
		- is it a diagram from decentralized to centralized
		- sees it as ecosystem map
		- would you still interact with gitlab and github
			- are they related to how he's working
- footer
	- PROJECT ID MISSING
	- ipns should be human readable is confused by that
	- likes the scuttlebot link
	- like IRC, mastodon
	- would open github and twitter in tabs +  radicle stack and intro guide
- goes to github radicle readme
- checks out oscoin as a org and browses throug repos
- goes to twitter, likes the flowers
- follows and lots of people they know
- goes to docs
	- scrolls through
	- long page with anchors
	- goes back to top and starts to read
	- go to the tutorial
	- goes to install
	- copy pastes & goes to terminal
		- installs radicle with homebrew
		- liked the cli in the browser of the old website
		- like the fact that there are a lot of stuff in the browser now
		- Would be up for installing things on his computer
			- doesn't demo everything, but knows the company
			- doesn't want to always install a whole thing
			- would only if there
		- is installing
		- wonders if it's gonna conflict with the other ipfs stuff that breaks sometimes
		- is confused by the 'launchd' word and doesn't want to to run all the time
		- doesn't know what daemon to run
		- doesn't know if its always gonna run in the background
		- Cory prompts him to look at background processes section
			- understands that brew services start will start something that is already installed
			- is gonn split his panes and run the daemons
			- would not use brew cause it installs a ton of stuff via brew, doesn't like npm , prefers npx which is cleaner
				- wonders if brew services does the same
			- would have like to read the background processes part, cause then he wouldn't have used brew
			- is bit confused by it all now
		- start the daemons without brew services
		- created the keys
		- OSX section
			- confirm what is isntalled through rad -help before brew services, and give alternative to run the daemons manually
			- would like to know why to have brew services in stead of manual daemons
		- goes to inspect the key file
			- expects a identity
			- hash in public key in ethereum is user id
			- is excited for ens
				- human readable public keys
				- urbit project
				- having an identity in a community is important part of a community
				- and having identity connected to security is nice in decentralized
				- feels strong desire to have identity connected to key
		- garden
			- who am i collaborating with?
			- would like the commands be code block (on guide ) rad diff porject and issue
			- is now in tilde town and is looking into that
				- no ssl
			- gets the goal of garden
			- runs rad help to see that it's installed
			- 'render output hosted found' is wrong
			- garden link is broken
			- **finally** understand what a radicle project is (issues is part of it) - is a problem he has at his company - backs up issues in his company (by prepper)
				- thought it was still a git repo, didn't understand everything is in the same project - thought it was torrenting of git files
				- "proposals" is unclear (might have to be diffs or PR , special issue?)
			- project ID is ugly
			- **create a folder??** before checkout?
			- would be nice if it told him it is clone
			- deosnt' know what a **proposal chain** is
			- rad issue list
			- "Diff proposal .." is confusing
			- issues are confusing cause there are 2 issues in cli but not in guide
			- want to make issues with markdown on github and preview the issues markdown in github, doesn't like this flow
			- adds a comment
				- doesnt' show up in show
				- doesnt' understand why if he adds it locally
			- **too many "now's"**
			- is taking an existing garden and editing it
			- **git add .**
			- HEAD on current one should be default (rad diff propose)
			- Unsure: diff means push? diff should be like a difference between 2 files
			- Would appreciate a brief overview comparing rad and git (..)
			- is confused by propose (thought it was a push so other see his branch) but now it's proposed to master and didn't get that it's
	- tutorial 2:
		- "..., however..." is confusing but

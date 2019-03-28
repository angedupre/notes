# Dogfooding issues

## Why

Even tough so far we've decided to not ship issues with the alpha release, we feel that we need to start moving some of our code collaboration over to radicle as soon as possible. The reason we do this is to allow ourselves to understand and identify the painpoints of building usable products with radicle. This will be important when we can start building [diff](../diff/diff-ux-flows.md) & git, our first radicle apps we want to ship with our alpha release (Feb 1, 2019).

## What

We've decided to do a 1 week deep dive (until Thursday 13th of December), executed by Merle, James & Julian around a predefined & aggreed upon scope, inspired by the work of Thomas that he defined [here](./issue-ux-flows.md).

The first priority is to make the issues chain usable for the radicle team, quickly followed by letting anybody create a chain and enabling more of us to use this.

## Scope

*Note* Issue 127 in the `radicle-issues` chain is where we're gathering feedback on the whole issues chain and CLI.

### Dogfood

- [x] _Creating issue_: This works, except that now the url is pointing to localhost.
- [x] _Unified CLI_
- [x] _CLI Help_
- [x] _Listing issues_: Julian is working on this right now.b
- [x] _Commenting_: Conversation over lunch suggests when you see an issue, everything is commented
      out, and anything you write outside of comments is a comment (lol). (A la git
      commit)
- [x] _Tutorial/setup guide_: I think for now the mixture of our current "Getting Started" and an email will do
- [ ] _Close issue_: This involves some CLI way of editing issues (cf. also below)
- [ ] _Notifications of new comments_: Or if an issue has been modified in some way. We can either store locally the latest info one has, and show changes, or as Merle suggested make it easier to find new things by timestamp.

### Post-dogfood

- [x] _Create a chain_: Otherwise the only people dogfooding are Thomas, James, Merle and I.
      to. (I think this is a lower priority and would be okay to skip.)
- [x] _Auth_
- [ ] _Editing issue_
- [ ] _Use local config.rad_: Which exposes e.g. the chain url to use.
- [ ] _fzf issue preview_
- [ ] _Install in PATH_

### Open questions

> I have a spare rasberry Pi, instead of using all its hashpower to make millions I was wondering if we can setup a radicle node for dogfood day? That would be a work stream I'd be very much interested to explore if it makes sense.

Thanks Onur. At the moment there are no concrete plans for standalone radicle nodes. We will have radicle nodes running on peoples machines that host Radicle State Machines and can be controlled by the user. So it makes only sense to run these nodes if you actively control them.

But we are also thinking about replication nodes that can be run stand alone. If we have something I’ll get back to you so we can try to set it up. I think we’ll learn a lot about how to package and manage the nodes.

# rad-issues

## Prerequisites:

Make sure you have fzf installed: https://github.com/junegunn/fzf

## Set up

Set up your default editor in your terminal. For better visuals use one that supports markdown previews. Otherwise issues will be opened
with `nano`:

    export EDITOR=<preferred-editor>

To set up the paths for the executables:

    export PATH=~/.local/bin:$PATH

These two lines only take effect for a single terminal session. To make them permanent (if you're using bash, the default), do:

    echo 'export PATH=~/.local/bin:$PATH' >> ~/.bashrc
    echo 'export EDITOR=<preferred-editor>' >> ~/.bashrc

## Installing the radicle stack

Install `stack` with:

    curl -sSL https://get.haskellstack.org/ | sh

Download and build the source code with:

    git clone https://github.com/oscoin/radicle.git
    cd radicle
    stack install radicle:exe:radicle

The stack is now installed and ready to be used.

## Using radicle-issues

_All commands below have to be made in the `radicle` directory as well._

Create a key & connect it to your username:

    bin/rad-issues make-key <username>

To get started run:

    bin/rad-issues help

Which in turn will give you this:

    rad-issues - Radicle issue CLI

    Usage:
        rad-issues [list|new|create-chain] <chain-name>
        rad-issues make-key <nick>
        rad-issues names
        rad-issues help

      list         - Select from all issues to view or comment on
      new          - Create a new issue in $EDITOR
      create-chain - Create a new issues chain
      make-key     - Create a key-pair and register the name
      names        - See all registered names
      help         - Print this help and exit

    If <chain-name> begins with 'http://', that URL will be used. Otherwise,
    http://machines.radicle.xyz/chains/ will be prepended to <chain-name>.

## Running your own server

For the purposes of the demo, and dogfooding, we're using the server that Thomas set up, so no one needs to do it themselves. If you want to play around with a toy chain, you can always use some improbable name.

But if you want to try your own local server:

    stack build radicle:radicle-server
    stack exec radicle-server

Note that by default (unless chain names begin with "http://"), the CLI uses Thomas' server. If you want to run the CLI against a local server, you need to use the full URL rather than just chain name. E.g. `bin/rad-issues list http://localhost:8000/chains/rad-issues` instead of just `bin/rad-issues list rad-issues`.

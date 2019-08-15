# An experimental tezos command line interface

This is an experimental project.

The `tez` program is a command line interface (CLI) for interacting with the Tezos blockchain.

## Goals (not necessarily implemented yet!)

* Easy to install on any popular operating system (binaries for all OS, packages for most, and docker images)
* A joy to use, makes use of the "sub-command" cli pattern that we have come familiar with (thanks git, docker, etal.)
* Ships with command completions for bash, zsh and powershell
* Easily create and manage tezos "contexts" allowing the user to store settings for mainnet, alphanet and privatenets (for testing/dev)
* Support transactions such as;
  * Managing delegations
  * Transferring tokens
  * Voting
  * Deploying smart contracts

## But there's already an official tezos-client

Yes, and `tezos-client` is great! But it has some downsides, and diversity is a strength.

The Tezos blockchain ships with `tezos-client`, a complete tezos cli. Its written in OCaml (which we ❤️), it is well tested and complete.

`tezos-client` has some downsides, in that it is not terribly easy to package. Building standalone static binaries is probably possible, but doesn't appear trivial. `tezos-client` is relatively tightly coupled to the core tezos node.

For new-comers to Tezos, we think interacting with the Tezos Block chain from the command line interface has too much friction.

`tezos-client` has has opinions and idiosyncrasies. Frankly, we have come to like them, but newcomers to Tezos may not have the same patience as us.

We also may end up having alternative implementations of the Tezos Node in other languages (hello simplestaking team!). Think of these as Linux distributions to GNU/Linux, but Tezos node distributions for the Tezos Blockchain. When new nodes come along, this `tez` cli could support them and the RPCs/APIs that they implement.

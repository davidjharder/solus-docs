# Packaging Tools and Environment Setup

This page will guide you through setting up the tools and environments needed to build Solus packages.


## `system.devel` Components

Building packages requires the packages included the the `system.devel` component group. Install them all with:

`sudo eopkg install -c system.devel`

## Solbuild

`solbuild` is self-contained build environment that builds `.eopkg` packages. Install `solbuild` and the accompanying configuration. All solus packages are built using the [unstable] repository.

`sudo eopkg install solbuild solbuild solbuild-config-local-unstable`

?? Is there a reason to not have every user install with the local profile?

Next, initialize solbuild:

`sudo solbuild init`

## Packaging Directory

blah

## Arcanist

Arcanist is a command-line utility used to communicate with the [Development Portal]. Install it if you plan to contribute to the official Solus repositories.

`sudo eopkg install arcanist`

Link your development portal account to arcanist:

``` bash
arc set-config default https://dev.getsol.us
arc install-certificate
```

On the last step you will be given a unique link to log into the development portal, to create a `Conduit API Token`. This token is automatically stored at `~/.arcrc`. You can now use the `arc` command to communicate with the development portal.

## Setting up Packager file

blah

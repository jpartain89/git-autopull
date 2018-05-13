# Git-AutoPull [![Build Status](https://travis-ci.org/jpartain89/git-autopull.svg?branch=master)](https://travis-ci.org/jpartain89/git-autopull)

More or less a wrapper script for [@icefox's](https://github.com/icefox) [git-map](https://github.com/icefox/git-map).

Of which, [git-map](https://github.com/icefox/git-map) is an absolutely awesome script. Go use it!

## Installation

To install `git-autopull`:

```bash
git clone https://github.com/jpartain89/git-autopull.git --recursive
cd git-autopull
./git-autopull
```

Make sure the `--recursive` flag is listed, to include cloning the `git-map` repo. 

## Usage

This script is a wrapper script to automatically run:

```bash
git-map pull
git-map fetch --all
git map submodule update --init --recursive
```

from within one of your locally cloned git repos.

> Note: It HAS to be ran from within a git repo, else it'll close by error.

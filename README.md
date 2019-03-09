# Git-AutoPull [![Build Status](https://travis-ci.org/jpartain89/git-autopull.svg?branch=master)](https://travis-ci.org/jpartain89/git-autopull)

# Git-Auto

I have two scripts that expand upon [@icefox's](https://github.com/icefox) [git-map](https://github.com/icefox/git-map) script:

`git-auto` and `git-autopull`

`git-auto` is for quickly `add`ing, `commit`ing (with a simple, short commit message) and `push`ing. 

  There are plans on adding the ability to customize the commit message per-call of the command. 
  For now, if you want a different boilerplate message, you can get in the script and change it.
  
`git-autopull` is for those people (like me) who keeps all of their git repo parent directories on the same level on their computers. If you want to just run through all of the repo's and pull down the updates, `git-autopull` loops through all the git repo directories, `pull`ing, `fetch --all`ing, and `submodule update --init --recursive`ing. 

## Installation

To install the scripts - for now, I plan on having a real install script - all you have to do is run it from within the `git clone`d location. It'll auto-link to `/usr/local/bin` directory.

```bash
git clone https://github.com/jpartain89/git-autopull.git --recursive
cd git-autopull
./git-autopull
./git-auto
```

Make sure the `--recursive` flag is listed, to include cloning the `git-map` repo. 

## Usage

### `git autopull`: It can be run with or without the `-` in the command. 
  
  Its primarily meant to be run from within a git repo directory, but you can combine other `git` command line flags along with `autopull`: 
  
`git -C ~/example/repo autopull` will run autopull in the `~/example/repo` directory level. 

### `git auto` requires at least a `.` to operate, because it requires a file location to operate.

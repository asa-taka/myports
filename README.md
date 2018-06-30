# myports

My dotfiles and home-made scripts preserver.

## [WIP] Installation

This tool uses git repository for contents presesrver.
So before use this tool, you shoud fork this repository
(make your own repository).

```sh
git clone https://github.com/<you>/myports ~/.myports
ln -s ~/.myports/myports* ~/bin
myports init
```

## Usage

Use [myports](./myports) to management your contents.

```
$ myports
Usage: myports <command> ...
Commands:
  diff    : 
  edit    : open myports directory by MYPORTS_EDTOR=code
  sh      : enter myports shell by MYPORTS_SH=bash
  pull    : pull updates to github
  push    : push updates to github

Usage: myports bin <command> ...
Commands:
  install : make symlinks of all dotfiles to MYPORTS_USER_BIN(=/Users/asa-taka/bin)
  list    : list dotfiles
  path    : print path
Note:
  Add 'export PATH=$(myports bin path):$PATH' to your profile to use your commands.

Usage: myports dotfiles <command> ...
Commands:
  install : make symlinks of all dotfiles 
  list    : list dotfiles
```
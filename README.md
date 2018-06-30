# myports

My dotfiles and home-made scripts preserver.

All features are now __Work in Progress, don't use__.

## Installation

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
Management user personal dotfiles and scripts
Usage: myports <command> ...

Commands:
  bin <subcommand>
          : management scripts, see 'myports bin help'
  commit  : 
  dotfiles <subcommand>
          : management dotfiles, see 'myports dotfiles help'
  edit    : open myports directory by MYPORTS_EDTOR=code
  sh      : enter myports shell by MYPORTS_SH=bash
  pull    : pull updates to github
  push    : push updates to github
  show-remote
          : show remote information

Note:
  Add 'export PATH=$(myports bin path):$PATH' to your profile to use your commands.
```
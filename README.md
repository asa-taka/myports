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

or you can select the other location to clone this repository.
If you do so, set `MYPORTS_DIR` as the correct path you installed.

## How it works

The aims of this tool is managing personal scripts and dotfiles
in remote git repositories.

### bin

Managing home-made scripts well.

Scripts are located on `$MYPORTS_DIR/bin` and it can be got by `myports bin path`.
Following shows the other utilities.

```
$ myports bin
Usage: myports bin <command> ...

Commands:
  install : make symlinks of all dotfiles to MYPORTS_USER_BIN(=)
  list    : list dotfiles
  path    : print path
  register <file>
          : register a script
  rm <script>
          : unregister a script
```

### dotfiles

Managing dotfiles under the `$HOME` directory.

dotfiles turn into symlinks of ones which managed by this(or your) git repository.
Once symlinks are created, you can sync your dotfiles easily.

```
$ myports dotfiles install
Create symlinks...
create /Users/asa-taka/.bash_profile -> /Users/asa-taka/.myports/dotfiles/.bash_profile
```

Following shows the other utilities.

```
$ myports dotfiles
Usage: myports dotfiles <command> ...

Commands:
  diff    : diff between preserved and installed
  install : make symlinks of all dotfiles 
  list    : list dotfiles
```

## myports: the management command

Use [myports](./myports) to management your contents.

```
$ myports
Management user personal dotfiles and scripts
Usage: myports <command> ...

Commands:
  bin <subcommand>
          : management scripts, see 'myports bin help'
  dotfiles <subcommand>
          : management dotfiles, see 'myports dotfiles help'
  edit    : open myports directory by MYPORTS_EDTOR=code
  env     : show configurable ENVs
  init    : clean all registered contents
  sh      : enter myports shell by MYPORTS_SHELL=bash
  pull    : pull updates from remote
  push    : push updates to remote
  show-remote
          : show remote information

Note:
  Add 'export PATH=$(myports bin path):$PATH' to your profile to use your commands.
```
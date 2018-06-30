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

## How it works

### bin

```
$ myports bin path
/Users/asa-taka/.myports/bin
```

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

dotfiles turn into symlinks of git managed ones.
Once symlinks are created, you can sync your dotfiles easily.

```
$ myports dotfiles install
Create symlinks...
create /Users/asa-taka/.bash_profile -> /Users/asa-taka/.myports/dotfiles/.bash_profile
```

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
  pull    : pull updates to github
  push    : push updates to github
  show-remote
          : show remote information

Note:
  Add 'export PATH=$(myports bin path):$PATH' to your profile to use your commands.
```
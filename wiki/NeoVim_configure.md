# NeoVim Configure

## Start

### Install NeoVim

```
brew install neovim
```

### Set default editor as nvim in terminal
```Shell
# .bash_profile
export EDITOR=
export EDITOR=/opt/homebrew/Cellar/neovim/0.7.0/bin/nvim 
``` 


### Open NeoVim

```
nvim
```

### Transitioning from vim
  1. To start the transition, create your `init.vim` (user config file:
```
:call mkdir(stdpath('config'), 'p')
:exe 'edit '.stdpath('config').'/init.vim
```

  2. Add these contents to the file:
```
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath = &runtimepath
source ~/.vimrc
```

  3. Restart Nvim. your existing Vim config will be loaded.

---


## Some tricks

### Change a first couple " to ' in selected rows

```
:nnorm 0cs"'
```

### Normalize the position in the near =

```
Tabularize /=
```

### Record macro definition

Record:

```
qa + some operations
```

Run:

```
@a
```


# Lazygit

### Open lazygit in a git repository
```command line
lazygit
```

### Open lazygit in different place
#### Ranger
1. Open `~/.config/ranger/rc.conf` 
2. Add mapping
```
# Open lazygit
map <c-g> shell lazygit
map <c-n> shell lazynpm
```

#### Shell: zsh
- Set alias `alias lg='lazygit'`
- Use ctrl + g
- 1. Open zsh
`cd ~/.config/zsh/mappings.zsh` 
- 2. Add fuctions
```Shell
function zle_eval {
    echo -en "\e[2K\r"
    eval "$@"
    zle redisplay
}

function openlazygit {
    zle_eval lazygit
}

zle -N openlazygit; bindkey "^G" openlazygit

function openlazynpm {
    zle_eval lazynpm
}

zle -N openlazynpm; bindkey "^N" openlazynpm
```

#### Neovim
Add mapping
```Vim
" Open up lazygit
noremap \g :Git
noremap <C-g> :tabe<cr>:tabmove<CR>:term lazygit<CR>
noremap <C-n> :tabe<cr>:tabmove<CR>:term lazynpm<CR>
```


### Lazygit Configuration
#### Install delta
```command line
brew install delta
```


### Basic interface
#### Basic command
- Select column: `h/l or <left>/<right>`
- View help: `x`


#### Common features
##### quick stage / unstage
- stage all: `a`    *like `git add .`*
- unstage all: `a`    *like `git reset`*
- stage / unstage a file: `<space>`
- stage / unstage a part: `<Enter>` and `<space>` select stage / unstage part
	- select stage window or unstage window: `<Tab>` 

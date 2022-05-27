# coc.nvim
### Install coc.nvim
#### Install node
```command line
brew install node
```

#### Install neovim and yarn
```command line
sudo npm i -g neovim yarn
```

#### Install coc by vim-plug
```command line
" Use release branch (recommend)
Plug 'neoclide/coc.nvim', {'branch': 'release'}

" Or build from source code by using yarn: https://yarnpkg.com
Plug 'neoclide/coc.nvim', {'branch': 'master', 'do': 'yarn install --frozen-lockfile'}
```

#### Install coc extension (eg: json)
```Shell
:CocInstall coc-json coc-tsserver
```

#### Uninstall coc extension (eg: json)
```Shell
:CocUninstall coc-json
```

#### View coc extensions
```Shell
CocList extensions
```

choose action: `<Tab>`
Exit: `<Esc>`

#### Automatically install coc extension
```Vim
let g:coc_global_extensions = [
	\ 'coc-json',
	\ 'coc-vimlsp'
	\ ...
]
```

<++>




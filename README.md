# waltobuddy.nvim

Waltified theme based on [bbenzikry/snazzybuddy.nvim]((https://github.com/bbenzikry/snazzybuddy.nvim)


Dark and light theme for Neovim using [tjdevries/colorbuddy.vim](https://github.com/tjdevries/colorbuddy.vim)

Based on [hyper-snazzy by sindresorhus](https://github.com/sindresorhus/hyper-snazzy), with inspiration from [snazzy light by lolio](https://github.com/loilo/vscode-snazzy-light) and [vim-snazzy by connorholyday](https://github.com/connorholyday/vim-snazzy)

<img width="695" alt="snazzybuddy_full" src="https://user-images.githubusercontent.com/1993348/113155528-c7599b00-9241-11eb-9cae-dc71b3e090e4.png">

*Font:* FiraCode Nerd Font

*Statusline:* [GalaxyLine](https://github.com/glepnir/galaxyline.nvim)

*RGB Highlighting:* [vim-hexokinase](https://github.com/RRethy/vim-hexokinase)


## Installation

```vim
" With Vim-Plug
Plug 'tjdevries/colorbuddy.nvim'
Plug 'waltjones/waltobuddy.nvim'

" Enable the color scheme
colorscheme waltobuddy
```

```lua
-- With packer
use 'tjdevries/colorbuddy.nvim'
use 'waltjones/waltobuddy.nvim'
```

```lua
--  in your lua config
require('colorbuddy').colorscheme('waltobuddy')
```


## Support for web-devicons
Built in support for web icons provided in [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons), commonly used with [nvim-tree](https://github.com/kyazdani42/nvim-tree.lua)

To enable colors for icons:

```vim
let g:snazzybuddy_icons = v:true
```

OR

```lua
vim.g.snazzybuddy_icons = true
```

## Use with [indent-blankline](https://github.com/lukas-reineke/indent-blankline.nvim)

```lua
-- Add SnazzyIndent1 - SnazzyIndent7
local indent_colors = {}
for i = 1, 7 do
    table.insert(indent_colors, 'SnazzyIndent' .. i)
end

vim.g.indent_blankline_char_highlight_list = indent_colors
```

## Switching between theme versions

```lua
function ThemeToggle()
    if vim.g.background == 'dark' then
        vim.g.background = 'light'
    else
        vim.g.background = 'dark'
    end
    require('waltobuddy').reload()
end

--- ... map this function to any keybinding
```


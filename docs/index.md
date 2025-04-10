# Setup

Inspired by <https://github.com/nvim-lua/kickstart.nvim>.

## Installation

1. Install Neovim>=0.11 (native LSP setup)
1. Install the external dependencies.
1. Clone this Git repository by replacing `<REPO>` with `<your_github_username>` in the commands below (Linux and Mac):

```sh
git clone https://github.com/<REPO>/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

## Plugins

I use the plugin manager [**lazy.nvim**](https://github.com/folke/lazy.nvim) to install all plugins. I also use [mini.nvim](https://github.com/echasnovski/mini.nvim) and [snacks.nvim](https://github.com/folke/snacks.nvim/tree/main?tab=readme-ov-file), two collections of plugins for Neovim.

✔️: finished setup and documentation.

❌: not setup properly and not documented.

### Working on text and code

| Name                                                                                          | Purpose                                                        | Dependencies                                                                                                                                                                         | Notes |
| --------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- |
| [blink.nvim](https://github.com/Saghen/blink.cmp)                                             | A completion plugin with support for LSPs and external sources |                                                                                                                                                                                      | ✔️    |
| [conform.nvim](https://github.com/stevearc/conform.nvim)                                      | Formatter plugin                                               |                                                                                                                                                                                      | ✔️    |
| [iron.nvim](https://github.com/Vigemus/iron.nvim)                                             | Interactive REPL (Read–Eval–Print Loop)                        |                                                                                                                                                                                      | ❌    |
| [mini.ai](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-ai.md)              | Extend and create a/i textobjects                              |                                                                                                                                                                                      | ✔️    |
| [mini.move](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-move.md#features) | Move any selection in any direction                            |                                                                                                                                                                                      | ✔️    |
| [mini.surround](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-surround.md)  | Fast and feature-rich surround actions                         |                                                                                                                                                                                      | ✔️    |
| [nvim-autopairs](https://github.com/windwp/nvim-autopairs)                                    | Autocomplete autopairs, e.g. [],{},() etc.                     |                                                                                                                                                                                      | ✔️    |
| [nvim-dap](https://github.com/mfussenegger/nvim-dap)                                          | Debug Adapter Protocol client implementation                   |                                                                                                                                                                                      | ❌    |
| [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)                         | Parser generator tool and incremental parsing library          | [nvim-treesitter-context](https://github.com/nvim-treesitter/nvim-treesitter-context), [nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects) | ✔️    |
| [snacks.indent](https://github.com/folke/snacks.nvim/blob/main/docs/indent.md)                | Adds indentation guides even on blank lines                    |                                                                                                                                                                                      | ❌    |
| [snacks.zen](https://github.com/folke/snacks.nvim/blob/main/docs/zen.md)                      | Zen mode, distraction-free coding                              |                                                                                                                                                                                      | ❌    |
| [todo-comments.nvim](https://github.com/folke/todo-comments.nvim)                             | Highlight your to-do comments in different styles              |                                                                                                                                                                                      | ❌    |
| [vim-sleuth](https://github.com/tpope/vim-sleuth)                                             | Smart indentation style detection                              |                                                                                                                                                                                      | ❌    |

### Working with files and navigating between files

| Name                                                               | Purpose                                                                                                             | Dependencies | Notes |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ------------ | ----- |
| [harpoon](https://github.com/ThePrimeagen/harpoon/tree/harpoon2)   | Auto updating and editable marks utility for fast file navigation                                                   |              | ❌    |
| [oil.nvim](https://github.com/stevearc/oil.nvim)                   | File Explorer that lets you edit your filesystem like a normal Neovim buffer                                        |              | ❌    |
| [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) | Fuzzy finder                                                                                                        |              | ❌    |
| [tmux](https://github.com/tmux/tmux)                               | Terminal multiplexer: it enables a number of terminals to be created, accessed, and controlled from a single screen |              | ❌    |

### Git Integration

| Name                                                        | Purpose                         | Dependencies | Notes |
| ----------------------------------------------------------- | ------------------------------- | ------------ | ----- |
| [gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim) | Deep buffer integration for Git |              | ❌    |
| [vim-fugitive](https://github.com/tpope/vim-fugitive)       | Vim plugin for Git              |              | ❌    |

### Miscellaneous

| Name                                                                                             | Purpose                                                          | Dependencies | Notes |
| ------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- | ------------ | ----- |
| [fidget.nvim](https://github.com/j-hui/fidget.nvim)                                              | Extensible UI for Neovim notifications and LSP progress messages |              | ❌    |
| [mini.icons](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-icons.md)           | File and folder icons                                            |              | ❌    |
| [mini.statusline](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-statusline.md) | Minimal and fast statusline module                               |              | ❌    |
| [which-key.nvim](https://github.com/folke/which-key.nvim)                                        | Show available keybindings in a popup as you type                |              | ❌    |

## Language Server Protocol, Debug Adapter Protocol, Linter and Formatter

The LSP (Language Server Protocol), DAP (Debug Adapter Protocol), Linter and Formatter will be installed by the package manager [Mason](https://github.com/williamboman/mason.nvim) (with dependencies: [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig), [mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim), [mason-tool-installer.nvim](https://github.com/WhoIsSethDaniel/mason-tool-installer.nvim), [mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)).

| Name                                                                   | Language             | Purpose                   | Notes                                                                                                                                                                                                                                                                             |
| ---------------------------------------------------------------------- | -------------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**debugpy**](https://github.com/microsoft/debugpy)                    | Python               | DAP                       |                                                                                                                                                                                                                                                                                   |
| [**harper_ls**](https://github.com/automattic/harper)                  | English :smile:      | Linter                    | Grammar Checker                                                                                                                                                                                                                                                                   |
| [**lua_ls**](https://github.com/LuaLS/lua-language-server)             | Lua                  | LSP                       | [lazydev.nvim](https://github.com/folke/lazydev.nvim) is a plugin that properly configures LuaLS.                                                                                                                                                                                 |
| [**prettier**](https://github.com/prettier/prettier)                   | JSON, Markdown, YAML | Formatter                 |                                                                                                                                                                                                                                                                                   |
| [**pyright**](https://github.com/Microsoft/pyright)                    | Python               | LSP                       | Need to install [Node.js](https://github.com/nodesource/distributions?tab=readme-ov-file#debian-and-ubuntu-based-distributions) because Pyright is written in Typescript. Ruff LSP will be an alternative to pyright [soon](https://github.com/astral-sh/ruff/discussions/16455). |
| [**ruff**](https://github.com/astral-sh/ruff)                          | Python               | LSP, Linter and Formatter |                                                                                                                                                                                                                                                                                   |
| [**stylua**](https://github.com/JohnnyMorganz/StyLua)                  | Lua                  | Formatter                 |                                                                                                                                                                                                                                                                                   |
| [**taplo**](https://github.com/tamasfe/taplo/tree/master)              | TOML                 | LSP, Linter and Formatter |                                                                                                                                                                                                                                                                                   |
| [**yamlls**](https://github.com/redhat-developer/yaml-language-server) | YAML                 | LSP                       |                                                                                                                                                                                                                                                                                   |

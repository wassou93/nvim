# Neovim Dot Files

This repository contains Neovim dot files for **wassou93**.

# Prerequisites

# NVIM v0.9.4 or later

### Quick Installation Guide

To install Neovim from a tarball and integrate it with your system, follow these steps:

1. **Download the Tarball:**
   Download the `nvim-linux64.tar.gz` tarball from [Neovim releases](https://github.com/neovim/neovim/releases).

2. **Extract the Tarball:**
   Extract the contents of the tarball using the following command:
   ```bash
   tar xzvf nvim-linux64.tar.gz
3. **Move to System Binaries:**
   ```bash
   sudo mv nvim-linux64 /usr/local/
4. **Create Symbolic Links:**
   ```bash
   sudo ln -s /usr/local/nvim-linux64/bin/nvim /usr/local/bin/nvim

## Rust
`curl --proto '=https' --tlsv2.2 -sSf https://sh.rustup.rs | sh`

## Rust Analyser
Install rust-analyzer:
`rustup component add rust-analyzer --toolchain stable`
You can also install rust-src for better debugging
`rustup component add rust-src`

## Node.js

- **nodejs**
  
   ```bash
    sudo apt install nodejs
    ```
- **npm**
  
   ```bash
    sudo apt install npm
    ```
   
## Tree-sitter

- Install tree-sitter

   ```bash
   sudo npm install -g tree-sitter
    ```

## EVCXR - Rust terminal Interpreter
Install using cargo:
`cargo install evcxr_repl`
You can also alias it with rust in `.bashrc`

# Installation

1. Clone this repository into the `Downloads` folder:

    ```bash
    git clone https://github.com/wassou93/nvim.git
    ```

    After cloning, copy the `nvim` folder to `~/.config`.

    ```bash
    cp -r nvim ~/.config/
    ```

    This ensures the configuration is in the correct location.

# Optional Installation Steps

1.Install Packer extension manager using below command:

> Unix, Linux Installation

```shell
git clone --depth 1 https://github.com/wbthomason/packer.nvim\
 ~/.local/share/nvim/site/pack/packer/start/packer.nvim
```

If you use Arch Linux, there is also [an AUR
package](https://aur.archlinux.org/packages/nvim-packer-git/).

2. Open `.config/nvim/` directory in neovim.
3. Press `q` mutliple times to ignore errors.
4. Press <leader>pv to return to nvim Explrer
5. Go to `./lua/wassou/packer.lua`
6. `:so` to source the file
8. Sync (add/update/remove) extensions:

    ```vim
    :PackerSync
    ```

9. Get installed Language Server Protocols (LSPs):

    ```vim
    :LspInfo
    ```

10. Install Language Server Protocols using Mason:

    ```vim
    :Mason
    ```

    - Scroll and press `i` to install the desired LSP server.
    - Ensure the backend is already installed on the system.

11. Enable transparency:

    ```vim
    :lua ColorMyPencils()
    ```

    This Lua command enables transparency.

# Troubleshooting

- If you're getting: `nvim-treesitter[vimdoc]: Error during compilation`
```bash
vi ~/.local/share/nvim/site/pack/packer/start/nvim-treesitter/lua/nvim-treesitter/shell_command_selectors.lua
```
- Add add `-std=c99` flag to `select_compiler_args` shown below in line 95:
  ```lua
   function M.select_compiler_args(repo, compiler)
  if string.match(compiler, "cl$") or string.match(compiler, "cl.exe$") then
    return {
      "/Fe:",
      "parser.so",
      "/Isrc",
      repo.files,
      "-Os",
      "/LD",
      "-std=c99", -- line 95
    }
   ...
  ```
Now, your Neovim setup is ready to go!

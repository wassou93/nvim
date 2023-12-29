# Neovim Dot Files

This repository contains Neovim dot files for **wassou93**.

# Prerequisites

To build Neovim from source, you need to have the following pre-requisites installed on your system:

- libtool
- autoconf
- automake
- cmake
- libncurses5-dev
- g++
- gettext

### Quick Neovim Installation Guide

To install latest Neovim, the best option is to build it from source and integrate it with your system, follow these steps:

1. **Remove previous nvim installations:**
   ```bash
   sudo apt remove neovim neovim-runtime
   sudo apt autoremove
   ```
3. **Clone the Neovim repository:**
   ```bash
   git clone https://github.com/neovim/neovim
   ```
4. **Navigate to the cloned repository:**
   ```bash
   cd neovim
   ```
5. **Checkout the stable branch:**
   ```bash
   git checkout stable
   ```
6. **Build Neovim:**
   ```bash
   make CMAKE_BUILD_TYPE=RelWithDebInfo
   ```
7. **Install Neovim:**
   - For Ubuntu/Debian based systems:
     ```bash
     cd build && cpack -G DEB && sudo apt install ./nvim-linux64.deb
     ```
   - For other systems:
     ```bash
     sudo make install
     ```

Note: The default installation location is `/usr/local`.

To uninstall Neovim, you can either run the following command:
```bash
sudo cmake --build build/ --target uninstall
```
Or delete the `CMAKE_INSTALL_PREFIX` artifacts:
```bash
sudo rm /usr/local/bin/nvim
sudo rm -r /usr/local/share/nvim/
```

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

# Neovim dot files 
Neovim dot files repo for --wassou93 

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

# Optional Prerequisites

## Node.js

- **nodejs**
  
   ```bash
    sudo apt install nodejs
    ```
- **npm**
  
   ```bash
    sudo apt install npm
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

1. Sync (add/update/remove) extensions:

    ```vim
    :PackerSync
    ```

2. Get installed Language Server Protocols (LSPs):

    ```vim
    :LspInfo
    ```

3. Install Language Server Protocols using Mason:

    ```vim
    :Mason
    ```

    - Scroll and press `i` to install the desired LSP server.
    - Ensure the backend is already installed on the system.

4. Enable transparency:

    ```vim
    :lua ColorMyPencils()
    ```

    This Lua command enables transparency.

Now, your Neovim setup is ready to go!

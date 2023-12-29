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

# Optional preprequisites

## Node
nodejs
npm

## EVCXR - Rust terminal Interpreter
Install using cargo:
`cargo install evcxr_repl`
You can also alias it with rust in `.bashrc`

# Installation
You can clone this repo in `Downloads` folder:
`git clone https://github.com/wassou93/nvim.git` 
Then copy the nvim folder to `~/.config`

# Optional installation steps
`:PackerSync` to sync (add/update/remove) extensions
`:LspInfo` to get installed LSPs
`:Mason` to install LSPs
You can scroll and press i to install the wanted lsp server
make sure backend is already installed in the system
`:lua ColorMyPencils()` to enable transparancy

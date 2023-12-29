# nvim
NVIM dot files

# Prerequisites
## NVIM v0.9.4 or later
## Rust
`curl --proto '=https' --tlsv2.2 -sSf https://sh.rustup.rs | sh`
## Rust Analyser
Install rust-analyzer:
`rustup component add rust-analyzer --toolchain stable`
You can also install rust-src for better debugging
`rustup component add rust-src`

# Optional preprequisites
# Node
nodejs
npm
# EVCXR - Rust terminal Interpreter
Install using cargo:
`cargo install evcxr_repl`
You can also alias it with rust in `.bashrc`

# Installation
You can clone this repo in `Downloads` folder:
git clone https://github.com/wassou93/nvim.git 
Then copy the nvim folder to `~/.config`

# Optional installation steps
`:PackerSync` to sync (add/update/remove) extensions
`:LspInfo` to get installed LSPs
`:Mason` to install LSPs
You can scroll and press i to install the wanted lsp server
make sure backend is already installed in the system
`:lua ColorMyPencils()` to enable transparancy

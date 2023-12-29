# nvim
NVIM dot files

# Prerequisites
## NVIM v0.9.4 or later
## Rust
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
## Rust Analyser
rustup component add rust-analyzer --toolchain stable
rustup component add rust-src

# Optional preprequisites
# Node
nodejs
npm
# EVCXR - Rust terminal Interpreter
cargo install evcxr_repl

# Installation
git clone https://github.com/wassou93/nvim.git 
After tthat copy nvim folder to `~/.config`

# Optional installation steps
:LspInfo to get installed LSPs
:Mason to install LSPs
you can scroll and press i to installed wanted lsp
make sure backend is already installed in the system
:lua ColorMyPencils() to enable transparancy

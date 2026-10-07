<h3 align="center">MacOS Dotfiles</h3>
<br>
<p align="center"><i>Personal configuration dotfiles for my MacOS environment. </i></p>

## About The Project

This repository contains my personal dotfiles, which are used to configure my development environment.

## Getting Started

To set up your environment with these dotfiles, follow the instructions below.

### Prerequisites

- Git

### Setup

To initialise the dotfiles repository in your home directory and set up Git to manage your dotfiles, use the following commands:

```bash
git init --bare $HOME/dotfiles-macos
alias config='/usr/bin/git --git-dir=$HOME/dotfiles-macos/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
config add <file>  # Replace <file> with the specific dotfile you want to track
config commit -m "Initial commit"
config push
```

### Update

To update your local dotfiles from the repository, use:

```bash
config pull
```

### New System

To set up your dotfiles on a new system, follow these steps:

```bash
git clone --bare git@github.com:ThousandEyedLibrarian/dotfiles-macos.git $HOME/dotfiles
alias config='/usr/bin/git --git-dir=$HOME/dotfiles-macos/ --work-tree=$HOME'
config checkout
```

### Notes

If you find any errors, issues, or have any questions, please feel free to either log an issue or [contact me](mailto:carterfs@proton.me).

### References

- [Atlassian Bare Repo Dotfiles](https://www.atlassian.com/git/tutorials/dotfiles)
- [FelixKratz/dotfiles](https://github.com/FelixKratz/dotfiles) - SketchyBar configuration this setup is based on (GPL-3.0)
- [LazyVim starter](https://github.com/LazyVim/starter) - Neovim configuration base (Apache-2.0)

### Licence

Copyright (C) 2023 Carter Facey-Smith. Released under the GPL-3.0 licence (see `LICENSE`). The Neovim configuration in `.config/nvim/` keeps its original Apache-2.0 licence.

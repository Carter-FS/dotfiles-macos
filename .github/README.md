# dotfiles-macos

Personal configuration dotfiles for my macOS environment: a tiling window manager setup whose hotkeys, borders and bar mirror my Omarchy setup on Arch ([dotfiles-arch](https://github.com/Carter-FS/dotfiles-arch)).

**Status:** Active

## What's included

- `.zshrc` - Oh My Zsh with aliases for eza, fzf and zoxide
- `.config/yabai/`, `.config/skhd/` - tiling window manager and hotkeys, with launch and toggle scripts
- `.config/sketchybar/` - status bar written in Lua (SbarLua)
- `.config/borders/` - Omarchy-style window borders (JankyBorders)
- `.config/nvim/` - Neovim, based on the LazyVim starter
- `.config/ghostty/`, `.config/starship.toml` - terminal and prompt
- `.gitconfig`, `.gitignore_global`, `.commit-conventions.txt` - git defaults and commit template

## Requirements

- macOS with [Homebrew](https://brew.sh)
- yabai, skhd, SketchyBar with SbarLua, JankyBorders, Ghostty, Neovim and Starship
- Oh My Zsh with zsh-autosuggestions, plus eza, fzf, bat and zoxide

## Setup

The dotfiles are managed as a bare git repository with `$HOME` as the work tree.

```sh
git clone --bare git@github.com:Carter-FS/dotfiles-macos.git $HOME/dotfiles-macos
alias config='/usr/bin/git --git-dir=$HOME/dotfiles-macos/ --work-tree=$HOME'
config config --local status.showUntrackedFiles no
config checkout
```

If `checkout` complains about existing files, back them up or remove them and run it again. After that, use `config` like `git`, for example `config pull` or `config add ~/.zshrc`.

## Credits

- [FelixKratz/dotfiles](https://github.com/FelixKratz/dotfiles) - the SketchyBar configuration this setup is based on (GPL-3.0)
- [LazyVim starter](https://github.com/LazyVim/starter) - the Neovim configuration base (Apache-2.0)
- [Atlassian bare repo dotfiles guide](https://www.atlassian.com/git/tutorials/dotfiles)

## Licence

Copyright (C) 2023 Carter Facey-Smith. Released under the GPL-3.0 licence (see `LICENSE`). The Neovim configuration in `.config/nvim/` keeps its original Apache-2.0 licence.

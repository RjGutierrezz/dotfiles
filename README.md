# Dotfiles
Personal macOS dotfiles for my daily development setup.
Managed with [GNU Stow](https://www.gnu.org/software/stow/) and organized by package so each tool can be linked into `$HOME` cleanly.

## Stack
- Shell: `zsh`
- Terminal: `ghostty`
- Multiplexer: `tmux`
- Editor: `neovim`
- Prompt: `starship`
- Window manager: `aerospace`
- System fetch: `fastfetch`

## Structure
Each folder is a Stow package.
```text
dotfiles/
  aerospace/
  fastfetch/
  ghostty/
  nvim/
  starship/
  tmux/
  zsh/
```

Examples:
- ghostty/.config/ghostty/... -> ~/.config/ghostty/...
- nvim/.config/nvim/... -> ~/.config/nvim/...
- zsh/.zshrc -> ~/.zshrc

Requirements
- homebrew
- macOS
- zsh
- git
- stow

Optional but expected for the full setup:
- ghostty
- tmux
- neovim
- starship
- aerospace
- fastfetch

Install
Clone the repo into your home directory:
git clone <your-repo-url> ~/dotfiles
cd ~/dotfiles
Stow packages individually:
stow zsh
stow ghostty
stow tmux
stow nvim
stow starship
stow aerospace
stow fastfetch

Or stow everything you want:
stow zsh ghostty tmux nvim starship aerospace fastfetch

Notes
- This repo is built around my personal macOS workflow.
- Some configs assume tools installed through Homebrew or standard macOS paths.
- Before stowing, remove junk files like .DS_Store.
- Keep package structure aligned with the final target path in $HOME.

Related Behavior
These configs are meant to work together:
- zsh loads starship, fastfetch, zoxide, conda, and nvm
- tmux and neovim share navigation/session workflow
- ghostty, tmux, and neovim are theme-aligned
- aerospace is used as the tiling window manager for the desktop workflow

Advice
If migrating existing configs into this repo:
- remove nested .git folders from imported configs if this will be a single repo
- avoid committing plugin clones, logs, caches, and OS metadata
- prefer tracking source config only, not generated files

License
Personal use unless stated otherwise.
```

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


## Requirements
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

## Install
You might need to install eveyrthing from homebrew first:
- JunkyBorders
brew tap FelixKratz/formulae
brew install borders
- Main applications
    - brew install ghostty
    - brew install tmux
    - brew install neovim
    - brew install starship
    - brew install aerospace
    - brew install fastfetch


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

## Disclaimer
- This repo is built around my personal macOS workflow.
- Some configs assume tools installed through Homebrew or standard macOS paths.
- Before stowing, remove junk files like .DS_Store.
- Keep package structure aligned with the final target path in $HOME.

## License
Personal use unless stated otherwise.

# Tolki's Dotfiles

## TL;DR

## Install dependencies

```sh
nix-env -iA nixpkgs.bitwarden-cli nixpkgs.chezmoi
```

## Setup chezmoi

```sh
bw sync
export BW_SESSION=$(bw unlock --raw)
chezmoi init mrtolkien
chezmoi apply
```

## Software list

Configures and installs:

- [`zsh`](https://www.zsh.org/)
- [`oh-my-zsh`](https://ohmyz.sh/)
- [`zsh-syntax-highlighting`](https://github.com/zsh-users/zsh-syntax-highlighting.git), [`zsh-autosuggestions`](https://github.com/zsh-users/zsh-autosuggestions), [`z`](https://github.com/agkozak/zsh-z), [`zsh-interactive-cd`](https://github.com/changyuheng/zsh-interactive-cd)
- [`fzf`](https://github.com/junegunn/fzf)
- Starship
- Nvim

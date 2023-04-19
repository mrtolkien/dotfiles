# Tolki's Dotfiles

## TL;DR

### Install `nix`

```sh
curl -L https://nixos.org/nix/install | sh -s -- --daemon
```

### CLI programs

```sh
nix-env -iA \
    nixpkgs.age \
    nixpkgs.atuin \
    nixpkgs.bat \
    nixpkgs.bitwarden-cli \
    nixpkgs.bottom \
    nixpkgs.chezmoi \
    nixpkgs.erdtree \
    nixpkgs.exa \
    nixpkgs.fd \
    nixpkgs.helix \
    nixpkgs.ripgrep
    nixpkgs.starship \
    nixpkgs.zoxide
```

### Setup chezmoi

```sh
bw sync
export BW_SESSION=$(bw unlock --raw)
chezmoi init mrtolkien
chezmoi apply
```

## Other `nix` installs

### CLI tools

## Flow

```mermaid
flowchart TD
    A(Install nix)
    AA("Install dependencies")
    B[( BitWarden CLI )]
    BB[[ 2FA with Authy ]]
    C("Setup dotfiles with chezmoi")
    D( Decrypt secrets with age )

    A --> AA --> C --> D
    AA --> B
    BB --> B --> D

    subgraph Bitwarden
        B
        BB
    end
```

## Software list

Configures and installs:

- [`zsh`](https://www.zsh.org/)
- [`oh-my-zsh`](https://ohmyz.sh/)
- [`zsh-syntax-highlighting`](https://github.com/zsh-users/zsh-syntax-highlighting.git), [`zsh-autosuggestions`](https://github.com/zsh-users/zsh-autosuggestions), [`z`](https://github.com/agkozak/zsh-z), [`zsh-interactive-cd`](https://github.com/changyuheng/zsh-interactive-cd)
- [`fzf`](https://github.com/junegunn/fzf)
- Starship
- Nvim

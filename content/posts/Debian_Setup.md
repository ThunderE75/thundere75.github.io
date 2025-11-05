+++
date = '2025-09-30T21:30:11+05:30'
title = 'My Debian Setup'
featured = true
tags= ['linux', 'guide']
description = 'My go-to tools and commands to set up a fresh Debian/Ubuntu system.'
+++

This is how i like to setup a fresh install of Debian (Ubuntu) based distributions.

# List of Tools
- {{<linkicon "https://github.com/volitank/nala" "fa-brands fa-github" "nala">}} - A front-end for apt (package manager)
- {{<linkicon "https://github.com/eza-community/eza" "fa-brands fa-github" "eza">}} - A modern replacement for ls
- {{<linkicon "https://github.com/ajeetdsouza/zoxide" "fa-brands fa-github" "zoxide">}} - A smarter cd written in rust
- {{<linkicon "https://github.com/ranger/ranger" "fa-brands fa-github" "ranger">}} - Console file manager with VI key bindings
- {{<linkicon "https://github.com/sharkdp/bat" "fa-brands fa-github" "bat">}} - A cat replacement with syntax highlighting and Git integration. 
- {{<linkicon "https://github.com/neovim/neovim" "fa-brands fa-github" "neovim">}} -  Vim-fork focused on extensibility and usability  
- {{<linkicon "https://github.com/jesseduffield/lazygit" "fa-brands fa-github" "lazygit">}} - A simple TUI for git  
- {{<linkicon "https://github.com/junegunn/fzf" "fa-brands fa-github" "fzf">}} - A general-purpose command-line fuzzy finder.
- {{<linkicon "https://github.com/aristocratos/btop" "fa-brands fa-github" "btop">}} - Resource monitor that shows usage and stats for processor, memory, disks, network and processes.

# Commands

- Updating the index and upgrading all the packages
- Installs the `nala` front end for apt & update the mirror

```sh
sudo apt update
sudo apt upgrade
sudo apt install nala
```

```sh
sudo apt install git curl exa zoxide ranger bat neovim fzf btop 
```

{{< callout type="info" title="Additional Steps Necessary" foldable=true collapsed=false >}}

You need to perform additional commands to install the following packages

- whyy {{% linkicon "https://github.com/jesseduffield/lazygit" "fa-brands fa-github" "lazygit" %}} no work

{{< /callout >}}

- Add my `alias.sh` file to `.bashrc`, this adds some Quality of Life Aliases

{{< highlight bat "style=xcode-dark">}}
cat << 'EOF' > ~/.alias
# ===== QoL Aliases =====
alias cls="clear"
alias vim="nvim"
alias cat="batcat"
alias f="fzf"
alias r="ranger"
alias z="zoxide"
alias refresh="source ~/.bashrc"

# ===== EXA Aliases =====
alias l="exa --icons --sort Name"
alias ls="exa --icons --grid --classify --colour=auto --sort=type --group-directories-first --header --modified --created --binary --group"
alias ll="exa --icons --sort Name --long --header"
alias la="exa --icons --sort Name --long --all --header"
alias lr="exa --icons --sort Name --long --recurse --header"
alias lra="exa --icons --sort Name --long --recurse --all"
alias lt="exa --icons --sort Name --long --tree --header"
alias lta="exa --icons --sort Name --long --tree --all"
EOF

grep -qxF 'source ~/.alias' ~/.bashrc || echo 'source ~/.alias' >> ~/.bashrc
source ~/.bashrc
{{< /highlight >}}

# Future Scope

- After a while, i usually switch to {{<linkicon "https://zsh.sourceforge.io/" "fa-solid fa-globe" "zsh">}} as my shell but i have not made my guide for it
- I use {{<linkicon "https://github.com/ohmyzsh/ohmyzsh" "fa-brands fa-github" "ohmyzsh">}} / {{<linkicon "https://github.com/ohmybash/oh-my-bash" "fa-brands fa-github" "oh-my-bash">}} to customize my prompt
- For ubuntu, i remove snap support & use {{< linkicon "https://flatpak.org/setup/Ubuntu" "fa-solid fa-box" "Flatpak">}}
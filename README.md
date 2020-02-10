# Ninetails dotfiles

Inspired on this video: [Screencast #1: How I manage my dotfiles with GitHub](https://www.youtube.com/watch?v=awtfkl50bUQ), by [Elliot Jackson](https://www.youtube.com/channel/UCX7q8yu2aY7AnwfoOeCEcgw)

## Manual Installation

```bash
pacman -S git
git init --bare $HOME/.dotfiles
alias dotfiles="git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME"
dotfiles remote add origin git@github.com:ninetails/dotfiles.git
dotfiles config status.showUntrackedFiles no
dotfiles fetch --all
dotfiles branch --set-upstream-to=origin/master master
dotfiles reset origin/master
dotfiles checkout -- .dotfiles
```

## Installation

```bash
wget https://raw.githubusercontent.com/ninetails/dotfiles/master/.dotfiles/scripts/init.sh -v -O /tmp/init.sh && chmod +x /tmp/init.sh && /tmp/init.sh && rm /tmp/init.sh
```

**DISCLAIMER** I am not responsible for any troubles by running this script.


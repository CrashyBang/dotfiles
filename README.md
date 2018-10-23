# dotfiles (WIP)
I control my dotfiles using [vcsh](https://github.com/RichiH/vcsh) and [myrepos](https://myrepos.branchable.com/).

My setup is largely based off these two articles [1](https://pikedom.com/managing-dot-files-with-vcsh-and-myrepo/) & [2](https://blog.tfnico.com/2014/03/managing-dot-files-with-vcsh-and-myrepos.html) with a few extra ease of life features added to help with setup.

The config repos contain **configuration files only** they do not include any instructions or scripts for installing the required binaries (i.e [neovim](https://neovim.io/), [zsh](http://www.zsh.org/), etc...) with the exclusion of the setup script which will install `vcsh` and `myrepos` if you are on an Ubuntu system. **If you are not on Ubuntu you will need to install these first**.

Quick start:
```
git clone https://github.com/CrashyBang/dotfiles.git  ~/.dotfiles && cd ~/.dotfiles && ./setup.sh
```

You can then delete this repository (`~/.dotfiles`) if you want as it really only servers as a bootstrapper, if not you can keep it around to quickly link additional configs that you may have left out during the setup, with:
```
~/.dotfiles/link.sh zsh
```
Where `zsh` is the config you would like to link (remember to run `mr update` after linking). 

### Configs (Need to add links)
- NeoVim
- Zsh
- Git
- Bin (Scripts)
- OpenBox

### Setup.sh (Needs to be created)
- [ ] Install `myrepos` and `vcsh`
- [ ] Clone down `config-mr` (using `vcsh`)
- [ ] Iterate over files `~/.config/mr/available.d` prompting creation of symlink in `~/.config/mr/config.d`
- [ ] Need to ignore `mr.vcsh` when iterating (this has to be linked - I think)
- [ ] Run `mr update`

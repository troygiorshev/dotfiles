# dotfiles
Personal dotfiles, courtesy of [Mackup](https://github.com/lra/mackup).

## To Restore

### Preliminaries

* Install zsh
* `chsh -s $(which zsh)`
* Reboot
* At zsh's first time startup (newuser-install), choose option 0
* Install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
* Install [Pure](https://github.com/sindresorhus/pure)
* Setup Python
  * Download [Miniconda](https://docs.conda.io/en/latest/miniconda.html#linux-installers)
  * `zsh Miniconda3-latest-Linux-x86_64.sh`
  * use .miniconda3 not miniconda3

### Mackup

* Clone this repo into ~/dotfiles
* `pip install --upgrade mackup`
* `ln -s ~/dotfiles/.mackup.cfg ~/.mackup.cfg`
* `mackup restore`

## Possible Issues

* Oh-my-zsh's "zsh completions" plugin might need to be fixed after a restore.

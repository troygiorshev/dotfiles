# dotfiles
Personal dotfiles, courtesy of [Mackup](https://github.com/lra/mackup).

## To Restore

### Preliminaries

* Install zsh
* `chsh -s $(which zsh)`
* reboot
* At newuser-install, choose option 0

### Mackup

* Clone this repo into ~/dotfiles
* Install Mackup
* `ln -s ~/dotfiles/.mackup.cfg ~/.mackup.cfg`
* `mackup restore`

## Possible Issues

* Oh-my-zsh's "zsh completions" plugin might need to be fixed after a restore.

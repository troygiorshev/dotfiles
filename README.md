# dotfiles
Personal dotfile backup, courtesy of [Mackup](https://github.com/lra/mackup).  
TODO: Consider upgrading to [rcm](https://github.com/thoughtbot/rcm)

## To Restore

### Preliminaries

* Install zsh
* `chsh -s $(which zsh)`
* Reboot
* At zsh's first time startup (newuser-install), choose option 0
* Install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
* Install oh-my-zsh packages, and others
  * `git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions`
  * `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting`
* Install [Pure](https://github.com/sindresorhus/pure)
* Setup Python
  * Download [Miniconda](https://docs.conda.io/en/latest/miniconda.html#linux-installers)
  * `zsh Miniconda3-latest-Linux-x86_64.sh`
  * folder: .anaconda3 not miniconda3
* Setup Screenfetch
  * `git clone https://github.com/troygiorshev/screenFetch.git ~/.zsh/screenFetch`
  * `sudo ln -s ~/.zsh/screenFetch/screenfetch-dev /usr/bin/screenfetch`

### Mackup

* Clone this repo into ~/dotfiles
* `pip install --upgrade mackup`
* `ln -s ~/dotfiles/.mackup.cfg ~/.mackup.cfg`
* `mackup restore`
  * Yes to all

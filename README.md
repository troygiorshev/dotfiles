# dotfiles
Personal dotfile backup, courtesy of [Mackup](https://github.com/lra/mackup).  
TODO: Consider upgrading to [rcm](https://github.com/thoughtbot/rcm)

## To Restore

### Preliminaries

* `sudo mkdir /usr/local/bin`
* Install zsh
* `chsh -s $(which zsh)`
* Reboot
* At zsh's first time startup (newuser-install), choose option 0
* Install [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)
  * `zsh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
* Install oh-my-zsh packages, and others
  * `git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions`
  * `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.zsh/zsh-syntax-highlighting`
* Install [Pure](https://github.com/sindresorhus/pure)
  * `git clone https://github.com/sindresorhus/pure.git ~/.zsh/pure`
* Setup Python
  * Download [Miniconda](https://docs.conda.io/en/latest/miniconda.html#linux-installers)
  * `zsh Miniconda3-latest-Linux-x86_64.sh`
  * folder: .anaconda3 not miniconda3
* Setup Screenfetch
  * `git clone https://github.com/troygiorshev/screenFetch.git ~/.zsh/screenFetch`
  * `sudo ln -s ~/.zsh/screenFetch/screenfetch-dev /usr/local/bin/screenfetch`
* Setup git's `diff-highlight`
  * `git clone https://github.com/git/git.git ~/.zsh/git`
  * `make -C ~/.zsh/git/contrib/diff-highlight`
  * `sudo ln -s ~/.zsh/git/contrib/diff-highlight/diff-highlight /usr/local/bin/diff-highlight`
* Mackup Restore (below)
* Fix irssi
  * In `.irssi/config` replace Freenode `sasl_password`

### Mackup

* `git clone https://github.com/troygiorshev/dotfiles.git ~/dotfiles`
* `pip install --upgrade mackup`
* `ln -s ~/dotfiles/.mackup.cfg ~/.mackup.cfg`
* `mackup restore`
  * Yes to all

## To Backup

* `mackup backup`
* `.irssi/config`
  * Redact Freenode `sasl_password`

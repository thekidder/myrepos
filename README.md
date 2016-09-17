### Instructions to bootstrap a new environment

#### (macOS) Grab brew

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

#### Bootstrap Homeshick

* `git clone git://github.com/andsens/homeshick.git $HOME/.homesick/repos/homeshick`
* `source "$HOME/.homesick/repos/homeshick/homeshick.sh`

#### Install myrepos

* macOS: `brew install myrepos`
* Ubuntu: `sudo apt-get install myrepos`

#### Finally, get config repos

`mr bootstrap https://raw.githubusercontent.com/thekidder/myrepos/master/home/.mrconfig`

#### Finish!

At this point you'll need to grab keys from another machine and place them in the correct place (`~/.ssh/identities/<identity_name>`). Then you can finish cloning private repos by running `mr update` (in a new shell to reload bashrc). You may also need to forcefully link castles once done: `homeshick link dotfiles hf-dotfiles myrepos`

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

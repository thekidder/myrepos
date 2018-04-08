### Instructions to bootstrap a new environment

### (Linux) Install git

`sudo apt-get install git`

#### (macOS) Grab brew

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

#### Bootstrap Homeshick

* `git clone git://github.com/andsens/homeshick.git $HOME/.homesick/repos/homeshick`
* `source "$HOME/.homesick/repos/homeshick/homeshick.sh"`

#### Install Java 8 JDK

* macOS: From the dmg at http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

#### Install some dependencies

* macOS: `brew install awscli jq node myrepos postgresql sbt supervisor vault`
* Ubuntu: `sudo apt-get install myrepos supervisor`

#### Finally, get config repos

`mr --trust-all bootstrap https://raw.githubusercontent.com/thekidder/myrepos/master/home/.mrconfig`

#### SSH keys and final myrepos setup

At this point you'll need to grab keys from another machine and place them in the correct place (`~/.ssh/identities/<identity_name>`). Then you can finish cloning private repos by running `mr update` (in a new shell to reload bashrc). You may also need to forcefully link castles once done: `homeshick link dotfiles hf-dotfiles myrepos`

#### Additional dependencies/tweaks

##### Python

* (macOS) Install brewed Python (with newer OpenSSL to work around old version in macOS): `brew install python`
* Setuptools and virtualenvs: `sudo easy_install pip && sudo pip install virtualenvwrapper`
* (macOS) You probably want to use the brewed python for new virtualenvs: ``mkvirtualenv -p `which python` NAME``

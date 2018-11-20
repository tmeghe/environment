# macOS environement setup
Personal notes about macOS development environment setup.

## Homebrew install
Homebrew setup

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### macOS High Sierra's permissions workaround

As found in this [Stack Overflow's post](https://stackoverflow.com/questions/46459152/cant-chown-usr-local-for-homebrew-in-osx-10-13-high-sierra)

```sh
sudo mkdir /usr/local/include
sudo mkdir /usr/local/Frameworks
sudo chown -R $(whoami) $(brew --prefix)/*
```

## Git install
Install git throught Homebrew

```sh
brew install git
```

### Global .gitignore
Create a global .gitignore file, which is a list of rules for ignoring files in every Git repository on your computer. For example, you might create the file at $~/.gitignore_global$ and add some rules to it.
```sh
git config --global core.excludesfile ~/.gitignore_global
```
The Octocat has a [Gist](https://gist.github.com/octocat/9257657) containing some good rules to add to this file.

## zsh Install

    brew install zsh
    sudo nano /etc/shells

The resulting `/etc/shells` file should look like this:

    /bin/bash
    /bin/csh
    /bin/ksh
    /bin/sh
    /bin/tcsh
    /bin/zsh
    /usr/local/bin/zsh

The `/usr/local/bin/zsh` location is the symlink Homebrew creates when installing zsh.

To actually change the shell assigned to the user account run

    chsh -s /usr/local/bin/zsh

The install oh-my-zsh

    sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

## install Powerline fonts

On other environments, you can copy and paste these commands to your terminal. Comments are fine too.
::
    # clone
    git clone https://github.com/powerline/fonts.git --depth=1
    # install
    cd fonts
    ./install.sh
    # clean-up a bit
    cd ..
    rm -rf fonts

## Ansible setup

```sh
sudo easy_install pip
sudo pip install ansible
```
Then create system wide Ansible directory with ```sudo mkdir /etc/ansible``` and copy the default Ansible configuration file
```bash
sudo curl -L https://raw.githubusercontent.com/ansible/ansible/devel/examples/ansible.cfg -o /etc/ansible/ansible.cfg
```

## Websocket management
WSCAT

# Organize things

* All code goes in *~/code*
* Inside *~/code* folder, projects follows **topic**, **platform** and **seriousness** paradigms

## Logs Managmenet

LNAV

License
----
MIT

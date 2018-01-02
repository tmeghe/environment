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

# Organize things

* All code goes in *~/code*
* Inside *~/code* folder, projects follows **topic**, **platform** and **seriousness** paradigms

License
----
MIT

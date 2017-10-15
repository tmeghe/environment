# macOS environement setup
Personal notes about macOS development environment setup.

## Homebrew install
Homebrew setup

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
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

# Dotfiles Management Using GNU Stow

This is for storage and management of my dotfiles. I am including my `zsh`, `nvim`, and `tmux` configuration directories and files.\
I am using [GNU stow](https://www.gnu.org/software/stow/) to manage my dotfile.

## Requirements

Ensure you have the following instaled on you system

### Git

###### Ubuntu
```
sudo apt-get install git
```

###### Arch
```
pacman -S git
```

### Stow

###### Ubuntu
```
sudo apt-get install stow
```

###### Arch
```
pacman -S stow
```

## Installation

First, clone the dotfiles repo to you `$HOME` directory using git.

```
$ git clone https://github.com/gerardo3022/dotfiles.github
$ cd dotfiles
```

Then create symlinks of the dotfiles to your `$HOME` directory.

``` bash
stow .
```

To care symlinks when a file already exists:
1. Create backup of the file `mv <FilePath>/<FileName> <FilePath>/<FileName>backup` (**Recommended**)
2. Overwrite changes `stow --adopt .`


## File Ignore List

There is already a [default list](https://www.gnu.org/software/stow/manual/html_node/Types-And-Syntax-Of-Ignore-Lists.html), but you can create a custom local list.\
Add names of files not to create a symbolic link of in the home directory in `.stow-local-ignore`.

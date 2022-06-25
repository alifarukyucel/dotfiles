# Dotfiles
This is a set of configuration files for bash, git, vim, and other applications that I use in my daily life. Feel free to use them if you'd like.

## Setup
Clone this repo into ~/.dotfiles and then run setup.sh.

## Packages

### Human Readable Format (HRF)
To list packages in a human readable format, run either of the following:

dpkg-query -l | less
apt list --installed # Human Readable Format (HRF)

### Export Packages
Exports all installed packages into packages_list.txt:

sudo dpkg-query -f '${binary:Package}\n' -W > packages_list.txt

### Import Packages
Installs all packages that are listed in packages_list.txt:

sudo xargs -a packages_list.txt apt install

# Dotfiles
This is a set of configuration files for bash, git, vim, and other applications that I use in my daily life. Feel free to use them if you'd like.

## Setup
Clone this repo into /home/{your_username}/.dotfiles and then run setup.sh.

## Packages

### Human Readable Format (HRF)
To list packages in a human readable format, run either of the following:

```dpkg-query -l | less```

```apt list --installed```

### Export Packages
To export all installed packages into packages_list.txt:

```sudo dpkg-query -f '${binary:Package}\n' -W > packages_list_verbose.txt```

### Import Packages
To install all packages that are listed in packages_list.txt:

```sudo xargs -a packages_list_verbose.txt apt install```

# Dotfiles
This is a set of configuration files for bash, zsh, git, vim, and other applications that I use in my daily life. Feel free to use them if you'd like.

## Setup
Clone this repo into ~/.dotfiles and then run setup.sh.

## Packages
List of manually installed packages is packages_list.txt
List of manually (+ automatically) installed packages is packages_list_verbose.txt

### Human Readable Format (HRF)
To list packages in a human readable format, run either of the following:

```dpkg-query -l | less```

```apt list --installed```

### Export Packages
To export all installed packages into packages_list_verbose.txt:

```sudo dpkg-query -f '${binary:Package}\n' -W > packages_list_verbose.txt```

### Import Packages
To install all packages that are listed in packages_list_verbose.txt:

```sudo xargs -a packages_list_verbose.txt apt install```

## Configurations for Programs
### VSCode
To export VS Code Extensions into vscode_extensions.txt in a re-installable format:

```code --list-extensions | xargs -L 1 echo code --install-extension > vscode_extensions.txt```

If vscode_extensions.txt already exists:

```cat vscode_extensions.txt | xargs -L 1 echo code --install-extension > vscode_extensions.txt```

### Firefox
Preferred profile configuration:

```.mozilla/firefox/xxxxxxxx.default/user.js```

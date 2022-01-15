# Dotfiles
This is a set of configuration files for bash, git, vim, and other applications that I use in my daily life. Feel free to use them if you'd like.

## List packages in a human readable format
dpkg-query -l | less
apt list --installed # Human Readable Format (HRF)

## List installed packages
sudo dpkg-query -f '${binary:Package}\n' -W > packages_list.txt

## Install packages on a fresh machine
sudo xargs -a packages_list.txt apt install

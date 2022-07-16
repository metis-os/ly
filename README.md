# metis-ly
// ly nerds login manager for @metis-os

A lightweight TUI (ncurses-like) display manager for [metis-os](https://metislinux.org), but yeah can easily be used with artix linux with runit.

Forked from [fairyglade's ly](https://github.com/fairyglade/ly) for [metis linux](https://metislinux.org) (runit).

![Metis Linux Login Screen with ly](https://user-images.githubusercontent.com/51807726/179344887-53addb56-29ce-4aed-9e3a-cc3593eba0dc.png)

So, you just have to [get this project](https://github.com/metis-os/metis-ly) and [it's runit service](https://github.com/metis-os/metis-ly-runit) and install them and enable the service.

Or, just get the packages (metis-ly and metis-ly-runit) from the [metis linux repo](https://github.com/metis-os/metis-repo) and install them with pacman and enable the service.

I don't know why but you need to remove the tty service to make ly work.

By default ly starts on tty2; so you need to remove agentty-tty2 i.e, `# rm -rf /run/runit/service/agetty-tty2`

You can change the config in /etc/ly/config.ini whenerver you change tty you need to remove the service for that specific tty.


## Dependencies
 - gcc
 - make (base-devel)
 - pam
 - xcb (libxcb)
 - xorg
 - xorg-xauth
 - mcookie (util-linux)
 - tput (ncurses)

### Tested and verified on metis linux with
 - dwm with xinitrc

# Gentoo deploy tools
===================

Tools to deploy gentoo stage3 & portage

## Installation

Install to $HOME/.gdt

    $ eval "$(wget -O- http://bit.ly/gdt-git)" 

##Usage example
Example use case tools

### Fast deploy

    $ export stage3=$(glist -s1)         #get stage3 url 
    $ export portage=$(glist -p/latest/) #get portage url
    $ mount /dev/sd[x] /mnt              #mount partition
    $ gstrap -s $stage3 -p $portage /mnt #download & extract stage3 & portage
    $ gchroot /mnt                       #join chroot enviroment

## Review

- **gmirror** Show and search gentoo mirrors.
- **gchroot** Preparing chroot enviroment. 
- **gstrap**  Download and extract stage3, portage archive.
- **glist** Show and search stage3, portage on selected mirros.

##License
![GPLv3](http://www.gnu.org/graphics/gplv3-127x51.png)

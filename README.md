# Gentoo deploy tools
===================

Tools to deploy gentoo stage3 & portage


## Installation

Install to /tmp

    $ wget http://bit.ly/gdt-install && source gdt-install

##Usage example
Example use case tools

### Fast deploy

    $ export stage3=$(glist -s1)         #get stage3 url 
    $ export portage=$(glist -p9)        #get portage url
    $ mount /dev/sd[x] /mnt              #mount partition
    $ gstrap -s $stage3 -p $portage /mnt #download & extract stage3 & portage
    $ gchroot /mnt                       #join chroot enviroment

###gmirrors

Show all gentoo mirrors available on http protocol

    $ gmirrors 

Show a line number

    $ gmirrors -n
    
Search mirror number 6

    $ gmirrors -s6

Search mirror regexp .ru/

    $ gmirrors -s/\\.ru\\//  # 

Show all gentoo mirrors available on http,ftp,rsynс protocol

    $ gmirrors -p http,ftp,rsynс


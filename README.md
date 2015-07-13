
# grub2-theme-gentoo
a grub2-theme for gentoo

based on https://github.com/LegendaryBibo/Steam-Big-Picture-Grub-Theme


## Screenshot 1600x900

<a href="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_1600x900.png">
   <img height=300 
   src="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_1600x900.png?raw=true">
</a>

<a href="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_terminal_1600x900.png">
   <img height=300 
   src="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_terminal_1600x900.png?raw=true">
</a>

## Screenshot 1280x1024

<a href="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_1280x1024.png">
   <img height=300 
   src="https://github.com/vitalogy/grub2-theme-gentoo/blob/master/screenshot/screenshot_1280x1024.png?raw=true">
</a>



## Reboot/Shutdown entry

edit /etc/grub.d/40_custom
```
#!/bin/sh
exec tail -n +3 $0
# This file provides an easy way to add custom menu entries.  Simply type the
# menu entries you want to add after this comment.  Be careful not to change
# the 'exec tail' line above.

menuentry "Reboot" --class reboot {
   reboot
}

menuentry "Shutdown" --class shutdown {
   halt
}
```
after that update grub (grub2-mkconfig -o ....)

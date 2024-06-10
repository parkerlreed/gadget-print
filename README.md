Demo video https://streamable.com/02rtwf

Steam Deck can work as a USB gadget. 

Assuming dual role device is enabled under BIOS

```
sudo modprobe g_printer
gcc -o prnt prnt.c
sudo ./prnt -read_data | ps2pdf - out.pdf && flatpak run io.mpv.Mpv ../prnt.mp3 && okular out.pdf
```

Code modified from https://www.kernel.org/doc/Documentation/usb/gadget_printer.rst

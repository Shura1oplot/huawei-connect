huawei-connect for Linux
========================

Huawei E3276 modem connect program.

This requires dhclient, usb_modeswitch, screen and pexpect python module.
On debian-like systems you can install it with:

```apt-get install usb-modeswitch screen python-pexpect```

Program has been tested with Russian operator Megafon on Ubuntu 12.04 and 13.04.

If modem doesn't work with usb 3.0, read this:
[launchpad bug 1094973](https://bugs.launchpad.net/ubuntu/+source/usb-modeswitch/+bug/1094973)
and [launchpad bug 979697](https://bugs.launchpad.net/ubuntu/+source/usb-modeswitch/+bug/979697)
or try execute with root privileges:

```echo "options usb-storage delay_use=3" >/etc/modprobe.d/usb-storage.conf```

and then reboot.

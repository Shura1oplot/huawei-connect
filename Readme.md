huawei-connect for Linux
========================

Huawei E3276 modem connect program.

It requires dhclient, usb_modeswitch, screen and pexpect module for python.
On debian-like systems you can install it with:

```# apt-get install usb-modeswitch screen python-pexpect```

Program was tested with Russian operator Megafon on Ubuntu 13.04.

Usage
-----

```
usage: huawei-connect [-h] [-v] [-a APN] [-m [MASK]] [-i SEC] [-d]

Huawei E3276 connect program

optional arguments:
  -h, --help            show this help message and exit
  -v, --version         show program's version number and exit
  -a APN, --apn APN     default apn is "internet"
  -m [MASK], --monitor [MASK]
                        monitor signal strength if connection is success
                        (default format is "\r{at} {ss_br} {op}{ld}"
  -i SEC, --interval SEC
                        interval in seconds between requests while monitoring
                        (default interval is 5)
  -d, --debug           print debug messages to stderr

MASK controls output. Interpreted sequences are:
  {ss_vl}   raw value of signal strength: 0..31 or 99
  {ss_dB}   signal strength in dB: -113..-51
  {ss_br}   signal strength bar: " ▂▄▆█"
  {ss_bi}   signal strength bar as number: 0..4
  {at}      access technology: 2G, 2G+, 3G, 3G+, 4G or unknown
  {op}      operator string
  {ld}      differences between length of last two lines in spaces
```

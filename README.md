CHIPSEC: Platform Security Assessment Framework
===============================================

[![Build Status](https://travis-ci.org/chipsec/chipsec.svg?branch=master)](https://travis-ci.org/chipsec/chipsec)

CHIPSEC is a framework for analyzing the security of PC platforms including hardware, system firmware (BIOS/UEFI), and platform components. It includes a security test suite, tools for accessing various low level interfaces, and forensic capabilities. It can be run on Windows, Linux, Mac OS X and UEFI shell. Instructions for installing and using CHIPSEC can be found in the [manual](chipsec-manual.pdf).

NOTE: This software is for security testing purposes. Use at your own risk. Read [WARNING.txt](chipsec/WARNING.txt) before using.

First version of CHIPSEC was released in March 2014:
[Announcement at CanSecWest 2014](https://cansecwest.com/slides/2014/Platform%20Firmware%20Security%20Assessment%20wCHIPSEC-csw14-final.pdf)

Recent presentation on how to use CHIPSEC to find vulnerabilities in firmware, hypervisors and hardware configuration, explore low level system assets and even detect firmware implants:
[Exploring Your System Deeper](https://www.slideshare.net/CanSecWest/csw2017-bazhaniuk-exploringyoursystemdeeperupdated)

Contact Us
----------

Mailing lists:

 * CHIPSEC users: [chipsec-users](https://groups.google.com/forum/#!forum/chipsec-users)
 * CHIPSEC developers: [chipsec-dev](https://groups.google.com/forum/#!forum/chipsec-dev)
 * [CHIPSEC discussion list on 01.org](https://lists.01.org/mailman/listinfo/chipsec)

Follow us on [twitter](https://twitter.com/CHIPSEC)

Note for Apollo Lake
--------------------

To use CHIPSEC in place without installing it:
python setup.py build_ext -i
sudo python chipsec_main.py

sudo python chipsec_util.py io list

sudo python chipsec_util.py io 0x80 byte 0x99

dump left lan poe ic
sudo python chipsec_util.py smbus read 0x40 0x00 0x100

turn off left lan poe power
sudo python chipsec_util.py smbus write 0x40 0x12 0xFC

turn on left lan poe power
sudo python chipsec_util.py smbus write 0x40 0x12 0xFF

dump right lan poe ic
sudo python chipsec_util.py smbus read 0x42 0x00 0x100

dump upper sodimm spd
sudo python chipsec_util.py smbus read 0xA4 0x00 0x100

dump bottom sodimm spd
sudo python chipsec_util.py smbus read 0xA0 0x00 0x100


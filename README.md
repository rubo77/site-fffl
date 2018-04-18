site-fffl
=========

This repository contains the site.conf and other configuration files for the Gluon-Firmware. For further Information (in German) please go to http://wiki.freifunk-flensburg.de/index.php?title=Gluon and read the article.

Changelog for Stable-Version "2017.1.6-1"
-----------------------------------------
Gluon specific changes:
* firmware based on gluon 2017.x commit:
https://github.com/freifunk-gluon/gluon/commit/a8af5c4499c23baa4a4e8d6c01828a7885739f37

FFFL specific changes:
* based on site-fffl commit:
https://github.com/freifunk-flensburg/site-fffl/commit/0c6808c21eca52a69f9fc30b2a9713b60e40376d +2
* removed ibss meshing, 802.11s mesh from now on only

Changelog for Stable-Version "2017.1.6-0"
-----------------------------------------
Gluon specific changes:
* firmware based on gluon 2017.x commit:
* https://github.com/freifunk-gluon/gluon/commit/a8af5c4499c23baa4a4e8d6c01828a7885739f37
* includes new gluon versions:
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.6.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.5.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.4.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.3.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.2.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.1.html
* https://gluon.readthedocs.io/en/latest/releases/v2017.1.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.7.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.6.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.5.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.4.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.3.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.2.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.1.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.2.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.1.6.html
* https://gluon.readthedocs.io/en/latest/releases/v2016.1.5.html
* https://gluon.readthedocs.org/en/latest/releases/v2016.1.4.html
* https://gluon.readthedocs.org/en/latest/releases/v2016.1.3.html
* https://gluon.readthedocs.org/en/latest/releases/v2016.1.2.html
* https://gluon.readthedocs.org/en/latest/releases/v2016.1.1.html
* https://gluon.readthedocs.org/en/v2016.1/releases/v2016.1.html

FFFL specific changes:
* based on site-fffl commit:
https://github.com/freifunk-flensburg/site-fffl/commit/40f76d37adcf16a794b0715e4b33a6cb6996278c +1 
* enable both ibss and 802.11s meshes for migration to 802.11s mesh only which will come in the next releases
* add 11s mesh_id "0x6666666c2d6d657368" which is hex and means "fffl-mesh" in ASCII
* removed alfred fromn site.mk
* add add "GLUON_REGION ?= eu"
* added static ntp servers 
* increased suggested outgoing bandwith-limit from 200kb/s to 400kb/s
* changed package name from gluon-announced to gluon-respondd
* added mlt's signing key to stable, beta and experimental branch 


Changelog for Stable-Version "2015.1.2-0"
-----------------------------------------
Gluon specific changes:
* firmware based on gluon 2015.1.x commit:
* xxx
* includes gluon versions:
* http://gluon.readthedocs.org/en/latest/releases/v2015.1.2.html
* http://gluon.readthedocs.org/en/latest/releases/v2015.1.1.html
* http://gluon.readthedocs.org/en/latest/releases/v2015.1.html

FFFL specific changes:
* based on site-fffl commit:
* https://github.com/freifunk-flensburg/site-fffl/commit/246df95045c048a608b6d8ac4fd3d59d2ef27f33
* removed public keys of wiflix, rene and flemming
* added public key of bigfoot
* modified structure of site.conf for compatibility with gluon 2015.1x
* modified site.mk GLUON_TARGET=ar71xx-generic  by default autoupdater on by default
* fastd mesh vpn peer limit from 2 to 1 to reduce background traffic

Changelog for Stable-Version "2014.4.0-0"
-----------------------------------------
* firmware based on gluon 2014.4.x commit c7687a2ae867c89d2c9906467b16e60a35d6e5f
* gluon-mesh-batman-adv-14
* added puplic keys from sven, horst, wiflix
* removed public keys from hendrik, drbob
* fastd method to salsa2012+umac for almost double vpn speed
* changed the version-naming to "gluonversion"-"ffflversion of that gluonversion"

Changelog for Stable-Version "S-1.1"
------------------------------------
* Added Public Key from Flemming for update signing
* Raised the number of valid signatures from 2 to 3 for beta and stable branch
* Added the Bugfix for the fastd-config-update Bug, see here: http://wiki.freifunk-flensburg.de/wiki/Fastd-bug

Changelog for Stable-Version "S-1.0"
------------------------------------
* IPv6-Prefix Changed from a Global-Prefix (2001:bf7:10:1::/64) to an ULA-Prefix (fddf:bf7:10:1::/64)
* Removed all Gateways from the site.conf exept "Snowden" and "Urbach"
* Added two new Gateways to the site.conf (gw01,gw02) with new public keys
* Changed next_node address to ULA-Prefix (2001:bf7:10:1::1 -> fddf:bf7:10:1::1)
* Changed fastd-port from 10000 to 10006
* Removed the update mirror "2001:bf7:10:1:1::3"
* Added the update mirrors "fddf:bf7:10:1:1::1" and "fddf:bf7:10:1:1::2"
* Shortend the release-name for the Stable-Versions
* The short Names are now for official stabel Versions only!
* Changed MTU to 1406

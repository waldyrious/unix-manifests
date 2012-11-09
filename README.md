unix-manifests
===============

Attempt at maintaining an updated list of [manifest files](http://en.wikipedia.org/wiki/Manifest_file)
(lists of all packages included in the distribution<sup>[1]</sup>) for popular Unix-like operating systems.
This list can be useful for tools to automatically calculate the (default) install base of a given software package.

For now, only the i386 architecture is included;
the patterns in the location and filename should be enough to infer the location
of the other architectures' manifest files.

**Legend:**
* ![text][]: text file
* ![archive][]: compressed text file (download and uncompress)
* ![in-cd][]: ISO CD image (donwload and mount/extract; path of manifest file is on the link text)

### **UNIX**

> ### **Linux**

> > _**Debian**_<sup>[2]</sup>: [debian-6.0.6-i386-DVD-1.list][debian] ![.gz][archive]

> > > Ubuntu: [ubuntu-12.04.1-desktop-i386.manifest][ubuntu] ![.manifest][text]

> > > > Mint: [casper/filesystem.manifest][mint] ![.manifest][in-cd]

> > > Knoppix

> > _**SlackWare**_

> > > OpenSUSE 

> > _**Arch**_

> > _**RedHat**_

> > > Fedora 

> > > > RHEL 

> > > CentOS 

> > > Mandrake/Mandriva 

> > > > PCLinuxOS 

> > > > Mageia 

> > _**Gentoo**_

> > _**Puppy**_

> ### **BSD** 

> > _**FreeBSD**_ 

> > > MacOSX 

> > _**NetBSD**_

> > > OpenBSD

[debian]: http://cdimage.debian.org/debian-cd/current/i386/list-dvd/debian-6.0.6-i386-DVD-1.list.gz
[ubuntu]: http://releases.ubuntu.com/precise/ubuntu-12.04.1-desktop-i386.manifest
[mint]: http://www.linuxmint.com/edition.php?id=103
[mint-bt]: torrents.linuxmint.com/torrents/linuxmint-13-mate-dvd-32bit.iso.torrent

[text]: http://upload.wikimedia.org/wikipedia/commons/7/75/Page_white.png "text file"
[archive]: http://upload.wikimedia.org/wikipedia/commons/d/d2/Page_white_zip.png "compressed text file"
[in-cd]: http://upload.wikimedia.org/wikipedia/commons/a/a0/Page_white_cd.png "cd image"

----
1. [These commands](http://www.datadisk.co.uk/html_docs/misc/unix_commands.htm#patch) could potentially work
   as an alternative, but first, I don't know how to make them display only non-user-installed packages,
   and second, one would need to have access to a instance of each system above to run those commands.
2. Debian includes ALL packages in its distribution.
   This means that the full Debian 6 fills over 50 CDs, or 8 DVDs.
   However, since they're ordered by popularity, often only the first CD or DVD is recommended for a first install.
   Here the first DVD will be considered a "standard install" of Debian.
   Note: The only medium that holds the whole thing in a single physical unit
   is a double-layer Blu-ray disc (DLBD).
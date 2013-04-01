unix-manifests
===============

The goal of this project is to maintain an updated list of [manifest files](http://en.wikipedia.org/wiki/Manifest_file)
(lists of all packages included in the distribution<sup>[1]</sup>) for popular Unix-like operating systems.

This list can be useful for various purposes; for example:
* as a starting point for the development of a multi-distibution package search app.
* as a resource for dependency management:
  a software project can use it to calculate the (default) install base of a given software package
  so that it can choose the dependencies that most people are likely to already have installed.
* as a starting point for [standardization efforts](https://lca2013.linux.org.au/wiki/Miniconfs/CrossDistributionLinux)
  regarding distribution manifest files, leading to greater transparency and user-friendliness.
* as a tool for choosing a distribution that commits to support/maintain the packages one is interested in.

For now, only the i386 architecture is included;
the patterns in the location and filename should be enough to infer the location
of the other architectures' manifest files.

**Legend:**
* ![text][]: text file
* ![archive][]: compressed text file (download and uncompress)
* ![in-cd][]: ISO CD image (donwload and mount/extract; path of manifest file is on the link text)  
<sub>[Images from Silk icon set: www.famfamfam.com/lab/icons/silk/ (CC-BY)]</sub>

### **UNIX**

> ### **Linux**

> > _**Debian**_<sup>[2]</sup>: [debian-6.0.7-i386-DVD-1.list][debian] ![.gz][archive]

> > > Ubuntu<sup>[3]</sup>: [ubuntu-12.04.2-desktop-i386.manifest][ubuntu] ![.manifest][text] /
                            [packages.ubuntu.com](http://packages.ubuntu.com/) ![search]

> > > > Mint<sup>[4]</sup>: [casper/filesystem.manifest][mint] ![.manifest][in-cd] /
                            [packages.linuxmint.com](http://packages.linuxmint.com/) ![search] ;
                            [community.linuxmint.com/software/search/](http://community.linuxmint.com/software/search/) ![search]

> > > Knoppix: [Packages.gz][knoppix] ![.gz][archive]

> > _**Slackware**_: [PACKAGES.TXT][slackware] ![.txt][text] /
                     [packages.slackware.com](http://packages.slackware.com/) ![search]

> > > OpenSUSE: [download.opensuse.org][opensuse] /
                [software.opensuse.org/search](http://software.opensuse.org/search) ![search]

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

[debian]: http://cdimage.debian.org/debian-cd/current/i386/list-dvd/debian-6.0.7-i386-DVD-1.list.gz 
[ubuntu]: http://releases.ubuntu.com/precise/ubuntu-12.04.2-desktop-i386.manifest
[mint]: http://www.linuxmint.com/edition.php?id=103
[mint-bt]: torrents.linuxmint.com/torrents/linuxmint-13-mate-dvd-32bit.iso.torrent
[knoppix]: http://debian-knoppix.alioth.debian.org/Packages.gz
[slackware]: http://mirrors.slackware.com/slackware/slackware-current/PACKAGES.TXT
[opensuse]: http://download.opensuse.org/

[logo]: https://raw.github.com/waldir/unix-manifests/master/unix-manifests.png
[text]: http://upload.wikimedia.org/wikipedia/commons/7/75/Page_white.png "text file"
[archive]: http://upload.wikimedia.org/wikipedia/commons/d/d2/Page_white_zip.png "compressed text file"
[in-cd]: http://upload.wikimedia.org/wikipedia/commons/a/a0/Page_white_cd.png "cd image"
[search]: http://upload.wikimedia.org/wikipedia/commons/7/79/Magnifier.png

----
1. [These commands](http://www.datadisk.co.uk/html_docs/misc/unix_commands.htm#patch) could potentially work
   as an alternative, but first, I don't know how to make them display only non-user-installed packages (update: check 
   [/var/log/installer/initial-status.gz](http://superuser.com/questions/48374/find-all-user-installed-packages)),
   and second, one would need to have access to a instance of each system above to run those commands.
2. Debian includes ALL packages in its distribution.
   This means that the full Debian 6 fills over 50 CDs, or 8 DVDs.
   The only medium that holds the whole thing in a single physical unit
   is a double-layer Blu-ray disc (DLBD).
   However, since the packages are ordered by popularity,
   often only the first CD or DVD is recommended for a first install.
   Here the first DVD will be considered a "standard install" of Debian.
   The full list can be obtained from
   [packages.debian.org/stable/allpackages](http://packages.debian.org/stable/allpackages?format=txt.gz).
3. A small number of the the packages listed here are removed after the instalation;
   see [here](http://askubuntu.com/questions/50077/how-to-get-a-list-of-preinstalled-packages#comment55698_50127).
4. A small number of the the packages listed here are removed after the instalation;
   Probably the final list is contained in the (binary) file `casper/filesystem.manifest-desktop` instead.
   Can anyone confirm this?

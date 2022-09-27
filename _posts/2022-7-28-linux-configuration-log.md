---
layout: post
title: Linux System Configuration And Log Files
subtitle: Inside The linux File System
cover-img: /img/posts/Linux-Log-Configuration/linux-Troubleshooting.jpg
thumbnail-img: /img/posts/Linux-Log-Configuration/linux-Troubleshooting.jpg
share-img: /img/posts/Linux-Log-Configuration/linux-Troubleshooting.jpg
tags: [Linux]
Comments: True
---

## Linux System Configuration And Log Files

*In previous article we learn what is Linux and its File system, New we are going to know about System Configuration and Log files.*

#### Lets Start the topic.

you will find descriptions of the configuration fi les you need to set up the different features that make up Linux systems. The two major locations of configuration fi les are your home directory (where your personal configuration fi les are kept) and the /etc directory (which holds system-wide configuration fi les). Most Important things for troubleshooting.

#### Linux System Configuration and log files

|File|Discription|
|-------|--------|
|/etc/sysconfig | Directory on Red Hat Linux that holds system configuration files|
|/etc/rc.d |Directory that holds system startup and shutdown files|
|/etc/rc.d/rcsysinit|Initialization file for the system|
|/etc/rc.config|Configuration file for SuSE Linux system|
|/etc/rc.d/rclocal|Initialization file for custom commands|
|/etc/rc.d/rcmodules|Loads kernel modules on startup of the system|
|/etc/rc.d/initd|Directory that holds many of the daemons, servers and scripts for the System V init startup control standard|
|/sbin/initd|Directory that holds many of the daemons, servers, and scripts for a SuSE system|
|/etc/rc.d/rc(1-8).d|Directories for the different runlevels; these directories hold  links to scripts in the /etc/rc.d/initd directory (on SuSE these are located in /sbin/initd/rc(1-8).d|
|/etc/rc.d/initd/halt|Operations performed each time the system is shut down Some distributions use the name rc.halt|
|/etc/rc.d/initd/lpd|Start up and shut down the lpd printing daemon|
|/etc/rc.d/init.d/inet|Operations to start and stop the inetd internet services daemon|
|/etc/rc.dfinit.d/nehvork|Operations to start and stop the network connections|
|/etc/rc.d/init.d/httpd|Operations to start and stop the httpd Web server daemon|
|/etc/X11|X Windows configuration files|
|/etc/lilo.conf|ULO configuration file|
|/etc/fstab|Listing of the Linux file systems and automatically mount file systems|
|/etc/hosts|Hosts configuration file|
|/mnt|Holds removable media file systems mount points|
|/etc/inittab|The default state and terminal connections|
|/etc/passwd|Contains user password and login information|
|/etc/shadow|Contains user-encrypted passwords|
|/etc/group|Contains a list of groups and the configuration for each group|
|/etc/syslog.conf|Contains the names and locations of system log files|
|/proc/|Contains hardware configurations of the system|
|/var/log/boot.log(x)|Show the completion of daemons and other system functions, (a) shows there are several corresponding to system boots
/var/log/cron (x)|Show the weekly and daily cron jobs completed, (.x) shows there are several corresponding to system boots|
|/var/log/dmesg|Contains hardware detected on boot up|
|/var/log/maillog (x)|Mail logs for system information, (.x) shows there are several corresponding to system boots|
/var/log/secure (x)|RSA key generation log, (1) shows there are several corresponding to system boot
|/var/log/spooler (x)|Spooler generation log, (.x) shows there are several corresponding to system boots|
|/var/log/fax|Directory of fax log files|
|/var/log/httpd|Directory of httpd Web daemon log files|
|/var/log/news|Directory of news daemon log files|
|/var/log/samba|Directory of samba log files|
|/var/log/squid|Directory of squid log files|
|/var/log/uucP|Directory of uucp log files|

This table provides a list of just some of the locations of important system files that you can use to configure and verify how the system is functioning. Knowing the location of the files and what they are used for will aid you in quickly troubleshooting a system when problems arise.
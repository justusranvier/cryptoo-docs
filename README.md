#Cryptoo

##Purpose of this repository

I've been using Gentoo Linux for years, and recently I've spent a lot of time improving the security of my system  as well as writing useful scripts and practices.

The purpose of these repositories is to document what  I've done  in case this information is useful to others, and also to help me with reproducing the setup in the future. Not to mention, that putting things in a public Git reposuitory will probably give me the incentive to clean things up a bit too...

##Project goals

My goal with this setup is to be able to run a variety of services on my  home network in as secure a manner as possible. 

Services such as Tor, I2P, Freenet, Bitcoin, Bitmessage, OpenVPN, and others.

I'd also like the devices on my home network to work well together, so that I can do things like log in from either my PC or my laptop and still have access to all my settings. This means using NFS to share my home directory, and also something Kerberos for passwords.

I'm becoming increasingly concerned about web browser security issues, so I'm also starting to add virtualization to my desktop as well, with multiple, purpose-segreated VMs containing the web browsers I use.

##Future goals

* Get Kerberos working again
* Implement SELinux
* Migrate from OpenRC to SystemD

##Host naming convention

Hostnames for physical and virtual machines are allocated from the element names (hydrogen, helium, lithium, beryllium, etc)

Ordering is mostly historical accident.

##Hardware description

###Phone

* Nexus 4
* Cyanogenmod

###Laptop PC

* Hostname: helium
* Acer Aspire 4830 upgraded with an SSD.
* Currently running Fedora instead of Gentoo because I don't use it very much and am not sure about how to set up power management efficiently.

###Server

* Hostname: lithium
* Intel(R) Core(TM) i7-3770K CPU @ 3.50GHz
* 32 GB RAM
* 10 hard drives, 2 TB each in RAID6 with 1 hot spares (~11 TB effective)
* Acts as NFS server for the LAN
* Host OS for most of the virtual machines, including all network-facing services.
* One of the virtual machines also acts as the external NAT/firewall

###Cable Modem

* Motorola SB6120
* Connects to lithium, and is managed by a firewall running inside a VM.
* Purchased out of pocket, because I wanted a cable modem that does **NOT** include a built-in wifi adapter
* http://web.mit.edu/newsoffice/2013/new-system-uses-low-power-wi-fi-signal-to-track-moving-humans-0628.html
* I do have a wifi access point too, but at least it's behing a firewall I control instead of being built into a device my ISP controls.

###Desktop

* Hostname: beryllium
* Intel(R) Core(TM) i7-2600 CPU @ 3.40GHz
* 16 GB RAM
* Most of my work is done here.
* Also acts as a virtualiztion host. I'm starting to move more of work into purpose-segreated VMs, although this machine probably needs more RAM before I go much further.


This is the high-level overview of the network. Other documents in this reposutory will provide more details about the exact virtualization and networking setup.

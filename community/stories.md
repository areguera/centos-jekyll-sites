---
title: "CentOS community stories"
title_lead: |
  The CentOS ecosystem has been built up with and around people. With no real
  commercial ambition we set out to try and solve problems for people as they
  exist in the sysadmin / operations trenches around the world.
layout: page
toc: true
---

This page will try and collect some of the user stories over the next few
months.  If you have one you'd like to offer up, get in touch with me at
[http://wiki.centos.org/KaranbirSingh](http://wiki.centos.org/KaranbirSingh).

## Major Hayden's story

I started with Linux in 1998 and my first distribution was Mandrake. My 
PowerPC machines (older Macs) ran Yellow Dog Linux and I really started 
to enjoy using YUP (YUM's predecessor).  I transitioned later to Gentoo 
Linux and spent quite a few sleepless nights testing the effects of USE 
flags as I compiled various software packages. Eventually, I stumbled 
upon some of the early Red Hat releases (prior to Enterprise Linux) and 
I enjoyed the ease of use and stability of the releases.  It seemed like 
so many other distributions were being pulled in multiple directions but 
the group working on Red Hat was highly organized.

When Red Hat switched to the Enterprise Linux model, I didn't have the 
large sums of money available to purchase the support licenses.  After 
all, I was just a college student at the time.  CentOS was a welcomed 
find and I was able to get it running quickly with my previous Red Hat 
knowledge.

Linux has always been enjoyable for me because I don't have to fork over 
large sums of money for Windows licenses on multiple machines. It's also 
really rewarding to teach other people how to use Linux-based operating 
systems and I love seeing the smiles on their faces when they see how 
much they can do with a free, open source operating system.

When I started at Rackspace six years ago, I worked in support and spent 
much of my time assisting customers with servers running Red Hat.  That 
led me to a position in our Cloud Servers product group as a Linux 
Engineer.  We worked through the Slicehost acquisition and eventually 
created a brand new cloud compute offering with OpenStack.  My 
contributions were a small part of what became The Rackspace Open Cloud 
servers product.  The knowledge we gained from operating such a large 
multi-tenant virtualization solution was poured into our new offering 
and we're excited to be working closely with the OpenStack community for 
features and bug fixes.  My focus has shifted a bit as the Chief 
Security Architect at Rackspace but I'm still a big fan of CentOS for my 
personal projects.

If you'd like to get in touch with me, find me on Twitter[1] or on IRC 
(mhayden on Freenode).  I've made plenty of posts regarding CentOS, 
Red Hat, and Fedora tips on my blog[2] and I maintain some Fedora/EPEL 
packages[3] that may be of interest.

1.  [http://twitter.com/majorhayden/](http://twitter.com/majorhayden/)
2.  [http://major.io/](http://major.io/)
3.  [https://admin.fedoraproject.org/pkgdb/users/packages/mhayden](https://admin.fedoraproject.org/pkgdb/users/packages/mhayden)

## Christoph Galuschka

My name is Christoph Galuschka - tigalch on IRC and in the fora - and I'm part of the CentOS QA team. I'm from Innsbruck, Austria, 36 years old and I'm working for a local utility company in their IT operations department. My responsibilities include VMware, everything VPN and firewall-related, the companywide internet access including security, and operating the company network. Previously to that I was working for an IT consulting company, which also operated its own WAN network to interconnect various customers. Apart from consulting I also handled most of the network related things (FrameRelay, ISDN- and ADSL-dialup, running internet related services like bind, apache, sendmail and the corporate firewall). As we also provided internet access and related services to our customers, we used Linux as the OS of choice for our servers. At was Slackware at that time, and OpenSuSE later. My first contact with CentOS was in 2007 or 2008. A company selling opengroupware.org as a ready to deploy collaboration server used CentOS5 as OS of choice.

Within the CentOS Project I'm doing QA. I'm also contributing to the wiki (German release notes) and the fora. Together with Athmane Madjoudj I'm also handling the t_functional stack (take a look at [http://ci.dev.centos.org](http://ci.dev.centos.org)) which helps us automate tests around CentOS-QA and Updates and the infra behind that setup.

At my current company we used to use OpenSuSE for various tasks i.e. syslog, rsync, local update repositories, internal firewalls or as base OS for virus scanners. The change in OpenSuSEs lifecycle policy forced us to reconsider the Distro of our choice, and so I recommended CentOS (C6 at that time). Within the time of 2 years I replaced almost every Linux installation (3 SLES servers are still left, but working on that) with CentOS6. Locking back, this was the right choice, which is proven by stability, easy applying of updates/point releases, manageability by using funcd and in general ease of use. Also the lifecycle expansion to 10 years and the joining of forces with RedHat are a big plus for CentOS in my view.

For the foreseeable future, the core SIG will probably be the part of CentOS in which I will be most interested/most used by me.

It is also looking like we will be deploying some more machines with CentOS6 at work, as running typo3 and wordpress is starting to pick up momentum there.


---
title: "The CentOS Variants"
title_lead: |
  A CentOS variant is a special edition of CentOS Linux that starts with the
  core distribution, then replaces or supplements a specific subset of
  packages. This may include replacing everything down to the kernel,
  networking, and other subsystems.
layout: page
permalink: /:path/:basename/index.html
toc: true
---

Some open source projects need different software components to run properly, such as updated development languages or kernel functionality. By being able to get these components directly in CentOS, a variant maintainer solves many of the steps for users.

The end goal is to make it easier for users to run different open source software directly on and in CentOS itself.

[Special interest groups](http://wiki.centos.org/SpecialInterestGroup) (SIGs) are teams of people interested in one or more related technologies, and enabling that technology in CentOS.

These SIGs want to get this technology in the hands of the users in the easiest way possible. SIG members usually include people who work directly on the related technology and open source projects.

(Some SIGs don't focus on producing a variant but instead work on Infrastructure, Design, Documentation, and so forth.)

## Using variants

It's as easy as using CentOS core. There are two main ways:

* Download a pre-built image [here](/download).
* Run the minimal installer from [here](/download) and choose your variant during installation.

You may want to look for additional tips, notes, and documentation in the [SIG that produces the variant](http://wiki.centos.org/SpecialInterestGroup).

<div class="alert alert-info" role="alert">
  <p class="h5 alert-heading"><i class="fas fa-edit"></i> <strong>Note:</strong></p>
  <p>The idea of CentOS Variants is very much a proposal at this stage,
  something we hope to have confirmed as a process and ensure we have resources
  allocated to make this happen by the early summer of 2014. However, if you
  are interested in joining the process right away, and dont mind being a part
  of the evolving process - feel free to drop a proposal for your variant onto
  the <a
  href="http://lists.centos.org/mailman/listinfo/centos-devel">centos-devel
  list</a> and we will try to include you in the process.</p>
</div>

Some potential early SIG's are listed on the [Special Interest Groups ](http://wiki.centos.org/SpecialInterestGroup).

## Making variants

An official variant edition of CentOS can only be created with code from git.centos.org, must be converted entirely from source to binary within the CentOS buildsystems and delivered using the official CentOS content delivery network.

The gateway to code getting in to git.centos.org is via the SIGs. For example, the SIG that maintains a variant or the core SIG that builds the main CentOS distribution.

You may want to join an existing SIG or start a new one if you have an idea for a completely new variant. [Read more about starting a SIG](http://wiki.centos.org/SpecialInterestGroup).

Of course, you are always permitted to remix and redistribute the CentOS code, but you need to read the [trademark guidelines](/legal/trademarks/) to know if you can call it "CentOS".

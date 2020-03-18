---
title: "The CentOS SIGs"
title_lead: |
  The Special Interest Groups (SIGs), are the teams responsible for their
  specific CentOS Project variants. Variants are specialized and focused rebuilds
  of CentOS to meet the needs and requirements of their corresponding communities
  and the technology associated with those communities.
permalink: /:path/:basename/index.html
layout: page
toc: true
---

SIGs are usually self-forming around a technology by a small community of
enthusiasts and interested parties. In addition to the existing CentOS SIGs, it
is expected that additional SIGs, as approved by the CentOS Board, will be
created.

Each group will be responsible for its own variant in CentOS that is
specifically targeted towards its community (e.g., The CentOS FooBar SIG
creates a CentOS variant targeted to FooBar users and developers, the CentOS
Hosting SIG builds a variant for web hosters, included in the CentOS
distribution). The SIG is the deciding authority on what is required in their
variant to satisfy the needs of their community, with the understanding that
the Board has ultimate oversight as explained elsewhere. If required, the
CentOS Board will help the individual SIGs to reach consensus on any issues or
problems.

SIGs are the only way for an entity to use and associate the CentOS brand with
a variant. You can always use Git and the repo to fork and try-out ideas, but
only those packages in git.centos.org and released and signed by CentOS can be
called 'CentOS'.

Another type of SIG is functional, focused on maintaining parts of the Project
itself, such as infrastructure, documentation, and design. A unique SIG is the
Core SIG that builds and maintains the core CentOS derivative of Red Hat
Enterprise Linux. It is unique because it is the central, orchestrating
platform that all other variants are built from.

## CentOS Core SIG Responsibilities

* Build the CentOS release.
* _Sign_ the CentOS release.
* Push official CentOS releases to the initial mirror.
* Coordinate with upstream as required.
* Accept changes into Git.
  * Manage Git licensing and contribution policies.

## Variant SIG Responsibilities

* Create and maintain one or more variations with technology in CentOS on top of or modifications to the core base.
* Foster a user community as a primary purpose of the variant.
  * Keep the Project artifacts (the variant) relevant and useful to the user community.
* Ensure the software brought in to support the variant is licensed and prepared properly for packaging and distribution as part of the CentOS Project.
* Oversee inclusions of code related to the variant in to git.centos.org.
* Conduct the business of the SIG following accepted open source practices around meritocracy and consensus decision making.

## Functional SIG Responsibilities
* Accountable for designing, building, and maintaining key Project component(s).
* Make the functional area open for participation, with barriers to contribution as low as feasible and reasonable.
* Foster a community of users and doers around the functional aspect, to share the responsibility, workload, and innovation.
* Work within given legal constraints and requirements.

## SIG Governance

<div class="captioned-image">
  <img class="img-responsive" src="/about/governance/sig-maturity-crossover.png" alt="Illustration" />
  <div class="caption">
    <p><i><!-- caption can go here --></i></p>
  </div>
</div>

The SIGs themselves also have a merit path toward autonomy and accountability
for Project aspects. The determination of merit level is reflected in the
amount of oversight required by the Board and the SIGs ability to self-sign and
release software builds. As merit increases, Board oversight goes down, with a
transition spot in the middle where the SIG naturally obtains more autonomy,
usually toward the end of the "Early" phase.

__Sandboxes__ are the entry point for all proposed SIGs. To enter, there must
be a Champion from or approved by the Board and a proposal (which indicates the
reason for the SIG, the expected audience, initial team, risks, etc.) For a SIG
to be created, there must be at least 3 +1 votes from the Board (NOT including
the Champion) and zero (nil) -1 votes. When approved, the Champion becomes the
formal Mentor of the Sandbox SIG.

Sandboxes cannot make formal releases, but can create releases that allow
people, developers, etc. to use, test, and play with the build. Sandboxes are
also closely monitored by the Board to ensure that they are attracting interest
and developers and users are learning the ropes regarding SIG operation. All
new committers, developers, SIG core team members, etc. must be approved by the
Board.

SIGs that have expressed a level of merit, as determined by the Board, will
move to the __Early__ SIG stage (Sandboxes can request graduation to Early, if
they like). These SIGs are allowed to create formal releases, but the release
must be approved by the Board and signed by the Mentor. In all other matters,
however, they are self-sufficient and no longer require Board approval, such as
as in adding committers and so forth. Movement from Sandbox to Early is via 3
+1 vote of the Board (Mentor not included) and zero (nil) -1 votes.

The final stage is the __Mature__ SIG. Again, this graduation is based on the
judgment and determination of the Board, but this movement must be a unanimous
decision of the Board. The Mature SIG has full control over the SIG, pulling in
its own sources to git.centos.org, its releases, its internal governance, and
has the ability to self-sign releases. The Board members may vote in, or
participate in any SIG decision at any time.

In both the Sandbox and Early SIGs, the role of the Board is primarily to
facilitate the movement of those SIGs towards the Mature level; it serves as an
initial gateway with the goal of getting out of the way of the SIGs.

Note that in all cases, maturity is a measure of the community itself, and not
the codebase or the actual SIG variant release. A mature SIG could create a
non-mature (e.g., Alpha or Beta release) distribution and, conversely, a
Sandbox SIG could produce a very mature (robust and reliable) distro.

## Community and SIGs

SIGs represent the true power and value of the CentOS Project. As seen in the
current CentOS Dojos, and in the CentOS community itself, the builds provide a
safe, neutral, and communal central meeting place for major technology areas.
This is the reason why SIGs should not be program/project specific (e.g., a
MariaDB rebuild), but rather technology-area focused (e.g., the "Hoster's"
rebuild). By creating a central point where all projects and communities can
interact, using the OS as the common foundation, upstream projects will be able
to reach and interface with a much larger audience.

It is expected that SIGs may propose significant forking of the base CentOS
core, such as introducing a new Python version or Linux kernel. It is the job
of the Board and CentOS Core SIG to oversee and approve any forks that are
pulled back into Git, including to ensure that these forks are supportable.
This support is best done by an active and engaged variant SIG. The Board or
CentOS Core SIG can pull a variant from release if they reasonably believe the
variant SIG is unable to support the variant. Another option is reassigning an
active variant from a dead SIG to a willing living SIG. The Board is
specifically not limited in what it can do to protect the quality of the CentOS
mark where it comes to the content and quality of a variant.

If you want to start a SIG please email the board at
[centosdev@centos.org](mailto:centosdev@centos.org) or
[board-requests@centos.org](mailto:board-requests@centos.org) for private
correspondence.

For the current list of active SIGs, refer to
[http://wiki.centos.org/SpecialInterestGroup](http://wiki.centos.org/SpecialInterestGroup)

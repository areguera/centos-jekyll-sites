---
title: "CentOS GPG Keys"
layout: page
toc: true
---

## How CentOS uses GPG keys
Each stable RPM package that is published by CentOS Project is signed with a GPG signature. By default, yum and the graphical update tools will verify these signatures and refuse to install any packages that are not signed, or have an incorrect signature. You should always verify the signature of a package prior to installation. These signatures ensure that the packages you install are what was produced by the CentOS Project and have not been altered by any mirror or website providing the packages. 

## Importing Keys
The Project GPG keys are included in the centos-release package, and are typically found in /etc/pki/rpm-gpg. Please note that not all keys in this directory are used by the CentOS project. Some keys may be placed in this directory by 3rd party repositories to enable the secure use of extra packages as well. The keys used by CentOS are enabled in the yum repository configuration, so you generally don't need to manually import them. 

If you want to verify that the keys installed on your system match the keys listed here, you can use GnuPG to check that the key fingerprint matches. For example:

    gpg --quiet --with-fingerprint /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
    pub  4096R/F4A80EB5 2014-06-23 CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>
      Key fingerprint = 6341 AB27 53D7 8A78 A7C2  7BB1 24C6 A8A7 F4A8 0EB5


## Project Keys
The following keys are currently in use by the CentOS Project. Please note that CentOS Linux releases may have several GPG keys assigned (depending on the release and architecture).
Worth knowing that for CentOS 8, there will be only one key that will be used for all architectures and also subsequent releases. SpecialInterestGroups (SIGs) will still use a different key though (see below)

### CentOS Project Keys (starting from CentOS 8)

#### CentOS Official Key
[download key](/keys/RPM-GPG-KEY-CentOS-Official)

	pub  4096R/8483C65D 2019-05-03 CentOS (CentOS Official Signing Key) <security@centos.org>
	Key fingerprint = 99DB 70FA E1D7 CE22 7FB6  4882 05B5 55B3 8483 C65D

#### CentOS Testing Key
[download key](/keys/RPM-GPG-KEY-CentOS-Testing)

	pub  4096R/5BA5FA8D 2019-05-03 CentOS Testing (CentOS Testing content) <security@centos.org>
	Key fingerprint = 793D 9072 6BF0 22DA E868  2C36 762E 6585 5BA5 FA8D

### CentOS-7 Keys

#### CentOS 7 Signing Key
[download key](/keys/RPM-GPG-KEY-CentOS-7)

    pub  4096R/F4A80EB5 2014-06-23 CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>
      Key fingerprint = 6341 AB27 53D7 8A78 A7C2  7BB1 24C6 A8A7 F4A8 0EB5

#### CentOS 7 Debug Key
[download key](/keys/RPM-GPG-KEY-CentOS-Debug-7)

    pub  2048R/B6792C39 2014-07-15 CentOS-7 Debug (CentOS-7 Debuginfo RPMS) <security@centos.org>
      Key fingerprint = 759D 690F 6099 2D52 6A35  8CBD D0F2 5A3C B679 2C39


#### CentOS 7 Testing Key
[download key](/keys/RPM-GPG-KEY-CentOS-Testing-7)

    pub  4096R/8FAE34BD 2014-06-04 CentOS-7 Testing (CentOS 7 Testing content) <security@centos.org>
      Key fingerprint = BA02 A5E6 AFF9 70F7 269D  D972 C788 93AC 8FAE 34BD


### CentOS 6 Keys

####CentOS-6 Signing Key
[download key](/keys/RPM-GPG-KEY-CentOS-6)

    pub  4096R/C105B9DE 2011-07-03 CentOS-6 Key (CentOS 6 Official Signing Key) <centos-6-key@centos.org>
      Key fingerprint = C1DA C52D 1664 E8A4 386D  BA43 0946 FCA2 C105 B9DE


#### CentOS-6 Debug Key
[download key](/keys/RPM-GPG-KEY-CentOS-Debug-6)

    pub  4096R/D0FF3D16 2011-07-03 CentOS-6 Debuginfo Key (CentOS-6 Debuginfo Signing Key) <centos-6-debug-key@centos.org>
      Key fingerprint = 69B3 0F26 BA2B 3AA4 C27C  E4F5 3B75 CF79 D0FF 3D16


#### CentOS-6 Testing Key
[download key](/keys/RPM-GPG-KEY-CentOS-Testing-6)

    pub  4096R/EF1D6DB8 2011-07-03 CentOS-6 Testing Key (CentOS-6 Test and Beta Signing Key) <centos-6-testing-key@centos.org>
      Key fingerprint = 4233 9C29 8BC4 352C A4F9  7504 119C 1A87 EF1D 6DB8

#### CentOS-6 Security Key
[download key](/keys/RPM-GPG-KEY-CentOS-Security-6)

    pub  4096R/FE837F6F 2011-07-03 CentOS-6 Security Key (CentOS-6 Official Security Key) <centos-6-security-key@centos.org>
      Key fingerprint = 0830 F43C 928A A5A8 A6F1  AF97 0B13 2C3F FE83 7F6F


### CentOS 5 Keys

#### CentOS-5 Signing Key
[download key](/keys/RPM-GPG-KEY-CentOS-5)

    pub  1024D/E8562897 2007-01-06 CentOS-5 Key (CentOS 5 Official Signing Key) <centos-5-key@centos.org>
      Key fingerprint = 473D 66D5 2122 71FD 51CC  17B1 A8A4 47DC E856 2897
    sub  1024g/1E9EA3B6 2007-01-06 [expires: 2017-01-03]

#### CentOS-5 Beta Key
    pub  1024D/092D7B2B 2007-01-06 CentOS-5 Beta Key (CentOS 5 Beta Signing Key) <centos-5-beta-key@centos.org>
      Key fingerprint = 5D82 2DFA 48B3 BE04 586C  BD4D CFDA 6881 092D 7B2B
    sub  1024g/DA743639 2007-01-06 [expires: 2017-01-03]


## Community Driven Project keys

The following keys are used to sign community led efforts within the CentOS Project ecosystem.

### SIG Keys

#### Atomic SIG
    pub  2048R/91BA8335 2015-06-10 CentOS Atomic SIG (http://wiki.centos.org/SpecialInterestGroup/Atomic) <security@centos.org>
    Key fingerprint = 64E3 E755 8572 B59A 3194  52AA F17E 7456 91BA 8335

#### ConfigManagement SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-ConfigManagement)

    pub   2048R/6E8B7E8A 2018-03-21 CentOS Config Management SIG (https://wiki.centos.org/SpecialInterestGroup/ConfigManagementSIG) <security@centos.org>
    Key fingerprint = C75A FB57 D5C0 F238 CB15  BEC8 1AE1 10FA 6E8B 7E8A

#### Cloud SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-Cloud)

    pub  2048R/764429E6 2015-05-15 CentOS Cloud SIG (http://wiki.centos.org/SpecialInterestGroup/Cloud) <security@centos.org>
    Key fingerprint = 736A F511 6D9C 40E2 AF6B  074B F9B9 FEE7 7644 29E6

#### NFV SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-NFV)

    pub   2048R/9D2A76A7 2018-02-20 CentOS NFV SIG (https://wiki.centos.org/SpecialInterestGroup/NFV) <security@centos.org>
    Key fingerprint = 736A F511 6D9C 40E2 AF6B  074B F9B9 FEE7 7644 29E6

#### OpsTools SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-OpsTools)

    pub  2048R/51BC2A13 2017-02-20 CentOS OpsTools SIG (https://wiki.centos.org/SpecialInterestGroup/OpsTools) <security@centos.org>
    Key fingerprint = 7872 8176 9AD7 3878 85EE  A649 4FD9 5327 51BC 2A13

#### Software Collections SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-SCLo)

    pub  2048R/F2EE9D55 2015-10-01 CentOS SoftwareCollections SIG (https://wiki.centos.org/SpecialInterestGroup/SCLo) <security@centos.org>
    Key fingerprint = C4DB D535 B1FB BA14 F8BA  64A8 4EB8 4E71 F2EE 9D55

#### Storage SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-Storage)

    pub  2048R/E451E5B5 2015-01-23 CentOS Storage SIG (http://wiki.centos.org/SpecialInterestGroup/Storage) <security@centos.org>
    Key fingerprint = 7412 9C0B 173B 071A 3775  951A D4A2 E50B E451 E5B5

#### Virtualization SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-Virtualization)

    pub  2048R/61E8806C 2015-06-17 CentOS Virtualization SIG (http://wiki.centos.org/SpecialInterestGroup/Virtualization) <security@centos.org>
    Key fingerprint = A7C8 E761 309D 2F1C 92C5  0B62 7AEB BE82 61E8 806C

#### PaaS SIG
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-PaaS)

    pub  2048R/2F297ECC 2016-05-18 CentOS PaaS SIG (https://wiki.centos.org/SpecialInterestGroup/PaaS) <security@centos.org>
    Key fingerprint = C5E8 AB44 6FA7 893D 7490  51F1 C34C 5BD4 2F29 7ECC

### AltArch keys

Community driven ports of CentOS to other platforms.

#### AArch64 Key
[download key](/keys/RPM-GPG-KEY-CentOS-7-aarch64)

    pub  2048R/305D49D6 2015-07-28 CentOS AltArch SIG - AArch64 (http://wiki.centos.org/SpecialInterestGroup/AltArch/AArch64) <security@centos.org>
    Key fingerprint = EF8F 3CA6 6EFD F32B 36CD  ADF7 6C7C B6EF 305D 49D6

#### Arm32 Key
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-AltArch-Arm32)

    pub  2048R/62505FE6 2015-11-27 CentOS AltArch SIG - Arm32 (https://wiki.centos.org/SpecialInterestGroup/AltArch/Arm32) <security@centos.org>
    Key fingerprint = 4D9E 39F1 499C A21D D289  77F8 CAFE F11B 6250 5FE6

#### PowerPC Key
[download key](/keys/RPM-GPG-KEY-CentOS-SIG-AltArch-7-ppc64)

    pub  2048R/F533F4FA 2015-11-27 CentOS AltArch SIG - PowerPC (https://wiki.centos.org/SpecialInterestGroup/AltArch) <security@centos.org>
    Key fingerprint = BAFA 3436 FC50 768E 3C3C  2E4E A963 BBDB F533 F4FA

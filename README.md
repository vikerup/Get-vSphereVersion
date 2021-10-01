# Get-vSphereVersion

## Getting started

Get-vSphereVersion is a simple way of verifying the current version of a VMWare vCenter Server.

### Usage

```
PS C:\> iex (new-object net.webclient).downloadstring("https://raw.githubusercontent.com/viksafe/Get-vSphereVersion/main/Get-vSphereVersion.ps1")

PS C:\> Get-vSphereVersion -servername 192.168.0.10


name          : VMware vCenter Server
fullName      : VMware vCenter Server 7.0.0 build-16386335
vendor        : VMware, Inc.
version       : 7.0.0
build         : 16386335
localeVersion : INTL
localeBuild   : 000
osType        : linux-x64
productLineId : vpx
apiType       : VirtualCenter
apiVersion    : 7.0.0.0
```

### VMware vCenter unauthenticated remote code execution CVEs

**CVE-2021-22005**

Fixed in:

* 7.0 Build 18356314
* 6.7 VCSA/Windows Build 18485166
* 6.5/6.0 not vulnerable

POC: https://github.com/r0ckysec/CVE-2021-22005

**CVE-2021-21972:**

Fixed in:

* 7.0 Build 17327517
* 6.7 VCSA/Windows Build 17138064
* 6.5 Build 17590285

POC: https://github.com/horizon3ai/CVE-2021-21972

**CVE-2020-3952:**

Fixed in:

* 7.0 not vulnerable
* 6.7 VCSA/Windows Build 15976714
* 6.5/6.0 not vulnerable

Note that vCenter must be in-placed upgraded from 6.0/6.5 to 6.7 to be vulnerable

POC: https://github.com/guardicore/vmware_vcenter_cve_2020_3952

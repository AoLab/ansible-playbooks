# DC
## Introduction
AIoTRC datacenter is located in Amirkabir CEIT datacenter. Following table describe the configuration of it.

| Host | IP | Users | Remote SSH Access | vCPUs | RAM | Name |
|:----:|:--:|:----- | :------------ | :----: | :---: | :---: |
| platform-base | 172.23.132.37 | parham | 50006 | 6 | 16GB | base.platform.site |
| platform-networking | 172.23.132.51 | parham | - | 4 | 8GB | ns.platform.site |
| platform-kube | 172.23.132.52 | parham | - | 8 | 24GB | kube.platform.site |
| platform-dev-1 | 172.23.132.50 | parham, sepehr | - | 8 | 8GB | dev1.platform.site |
| platform-dev-2 | 172.23.132.41 | parham | - | 8 | 8GB | dev2.platform.site |

The following URLs are assigned to AIoTRC:

- [platform, *.platform].ceit.aut.ac.ir --> 172.23.132.37
- backback.ceit.aut.ac.ir

Platform DNS is available on `platform-networking` and its configuration is available in `bind9`.
In order to use specific dns with dhcp on Ubuntu 18.04 check [this](https://askubuntu.com/questions/1001241/can-netplan-configured-nameservers-supersede-not-merge-with-the-dhcp-nameserve) stackoverflow question.

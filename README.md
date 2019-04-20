# DC
## Introduction
AIoTRC datacenter is located in Amirkabir CEIT datacenter. Following table describe the configuration of it.

| Name | IP | Users | Remote access (through SSH) | vCPUs | RAM |
|:----:|:--:|:----- | :------------ | :----: | :---: |
| platform-base | 172.23.132.37 | parham | 50006 | 6 | 16GB |
| platform-networking | 172.23.132.51 | parham | - | 4 | 8GB |
| platform-kube | 172.23.132.52 | parham | - | 8 | 24GB |
| platform-dev-1 | 172.23.132.50 | parham | - | 8 | 8GB |
| platform-dev-2 | 172.23.132.41 | parham | - | 8 | 8GB |

The following URLs are assigned to AIoTRC:

- platform.ceit.aut.ac.ir --> 172.23.132.37
- backback.ceit.aut.ac.ir

Platform DNS is available on `platform-networking` and its configuration is available in `bind9`.

# DC :wrench:
## Introduction
Aolab datacenter is located in Amirkabir CEIT datacenter. Following table describe the configuration of it.

| Host | IP | Users | Remote SSH Access | vCPUs | RAM | Name |
|:----:|:--:|:----- | :------------ | :----: | :---: | :---: |
| platform-base | 172.23.132.37 | parham | 50006 | 6 | 16GB | base.platform.site |
| platform-networking | 172.23.132.51 | parham | - | 4 | 8GB | ns.platform.site |
| platform-kube | 172.23.132.52 | parham | - | 8 | 24GB | kube.platform.site |
| platform-dev-1 | 172.23.132.50 | parham, sepehr | - | 8 | 8GB | dev1.platform.site |
| platform-dev-2 | 172.23.132.41 | parham | - | 8 | 8GB | dev2.platform.site |

The following URLs are assigned to Aolab:

- [platform, *.platform].ceit.aut.ac.ir --> 172.23.132.37
- backback.ceit.aut.ac.ir

And the following port mapping is avaiable for `platform.ceit.aut.ac.ir`:

- 50008 -> 8000

Platform DNS is available on `platform-networking` and its configuration is available in `bind9`.
In order to use specific dns with dhcp on Ubuntu 18.04 check [this](https://askubuntu.com/questions/1001241/can-netplan-configured-nameservers-supersede-not-merge-with-the-dhcp-nameserve) stackoverflow question.

## OpenVPN

In the `platform-base` there is a simple but useful openvpn service that operates on port 8000.
For better usage please use the following command in `ovpn` file:

```
# redirect-gateway def1
route 172.23.0.0 255.255.0.0
```

## I1820 Domain

To support `https` we use [Certbot](https://certbot.eff.org) on Ubuntu 18.04.
Please note that we use dns challenge with the following command:

```sh
brew install letsencrypt
sudo certbot certonly --manual -d '*.platform.i1820.org' -d 'platform.i1820.org' --preferred-challenges dns
```

I1820 monitoring is based on [uptime robot](https://uptimerobot.com).

## DNS
- Domain: i1820.org
- Registered with: [Iranserver](https://iranserver.com)
- Managed on: [ArvanCloud](https://npanel.arvancloud.com)

## Aolab Domain

## DNS
- Domain: aolab.org
- Registered with: [Iranserver](https://iranserver.com)
- Managed on: [ClouDNS](https://asia.cloudns.net)

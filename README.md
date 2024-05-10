# cutel-vgw-provisioning

This repo serves as the "top level" documentation and example for a number of ansible roles stored in other repos that allow you to provision Cisco VG202, VG204 and VG224 Voice Gateways for connection to a SIP server.

It is aimed at people that want to setup a [CuTEL](https://cutel.net/) style telephone network for fun.

## Features

- Erases the configuration and then bootstraps a voice gateway ready for a fresh config
- Configure Login authentication, VTYs, banners etc
- Configure FXS Ports, Dial Peers, SIP-UA, translation rule and other voice settings
- Force tromboning calls through the SIP server
-  Configure DNS, NTP, SNMP and Dynamic DNS
- Bridge the two  ethernet interfaces to enable switching / passthrough
- Configure Network Interfaces including static or DHCP IP addresses
-  Add a basic ACL to the primary ethernet interface

## Usage

Install the requirments  

`ansible-galaxy role install -r requirements.yml -f`

Run ansible  

`ansible-playbook -i inventory/inventory.yml -l vgw-110.cutel.dns.c26.uk,vgw-111.cutel.dns.c26.uk provision.yml`


## Disclaimers

This project was created for fun - using it for production / anything important is discouraged.  Updates are likely to happen in sporadic bursts or not at all, and bugs may occasionally get introduced. 

## Acknowledgments

Many thanks to [maxlock](https://github.com/maxlock) for coming up with the bootstrap process and ansible logic.

## Licence 

This project is licenced under GPL-3.0. See LICENSE.md for details
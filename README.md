# ansible-easy-vpn
![CI](https://github.com/swanserquack/ansible-easy-vpn-oci/actions/workflows/ci.yml/badge.svg)

A simple interactive script that sets up a Wireguard VPN server with Adguard, Unbound and DNSCrypt-Proxy on an Oracle Cloud instance, and lets you manage the config files using a simple WebUI protected by two-factor-authentication.

**Have a question or an issue? Read the [FAQ](FAQ.md) first!**

## Usage

```
wget https://raw.githubusercontent.com/swanserquack/ansible-easy-vpn-oci/main/bootstrap.sh -O bootstrap.sh && bash bootstrap.sh
```

## Features
* Wireguard WebUI (via wg-easy)
* Two-factor authentication for the WebUI (Authelia)
* Hardened web server (Bunkerweb)
* Encrypted DNS resolution with optional ad-blocking functionality (Adguard Home, DNSCrypt and Unbound)
* IPTables firewall with sane defaults and Fail2Ban
* Automated and unattended upgrades
* SSH hardening and public key pair generation (optional, you can also use your own keys)
* E-mail notifications (using an external SMTP server, e.g. GMail)

## Requirements
* An instance on Oracle Cloud Infrastructure with:
  * At least 1 vCPU
  * At least 1 GB RAM (2 GB recommended)
  * At least 10 GB of disk space
* One of the supported Linux distros (Only Ubuntu Server 24.04 has been officially tested):
  * Ubuntu Server 24.04 (recommended)
  * Ubuntu Server 22.04
  * Ubuntu Server 20.04
  * Debian 11
  * Debian 12

## Expectations
This repo is maintained **voluntarily**, I do run my own instance meaning that its continued development and maintenance is in my best interest. This repo is specifically designed to be for instances on Oracle Cloud, no other VPS providers are officially supported. Issues/Questions regarding other VPS providers will be marked as "won't fix" unless the issue is trivial to resolve, could affect Oracle Cloud or is of particular interest to me. 

Whilst I try my best, I cannot reproduce every possible VPS configuration. If you report an issue with a configuration that cannot be reproduced here, please help me solve it by providing one of the following: a minimal, reproducible set of steps and any relevant logs or configuration files; a through description of your configuration or temporary access to a test instance that reproduces the issue. 

Requests/Issues that require long-term or paid resources may be considered out of scope unless I find the request particularly interesting **and** have the resources to act upon it **or** an agreement is made to provide the resources needed to act upon it.
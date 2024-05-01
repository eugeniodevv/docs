---
sidebar_position: 0
title: "Setup"
---

# RemoteShield Setup

After ordering a [RemoteShield](https://neoprotect.net/remoteshield) service you will receive all
necessary details (tunnel endpoints, network config, etc.) through our team.

If you want to use [RemoteShield](https://neoprotect.net/remoteshield) with your **own IPs** (BYOIP) you
can take a look at our [IP Transit](/category/ip-transit) service.

## Establish a tunnel to our network

Take a look at one of our guides, depending on operating system and tunnel type:

- [GRE Tunnel on Linux](gre_linux.md)
- [GRE Tunnel on Windows](gre_windows.md)
- [IPIP Tunnel on Linux](ipip_linux.md)
- [IPIP Tunnel on Windows](ipip_windows.md)

If you have further questions don't hesitate to contact our [Support](../support.md).

## Edge Firewall setup

Our managed firewall allows you to create rules on our network edge, giving you full control of which
packets are passed to your tunnel endpoints.

You can create multiple rules for each destination IP with the following options:
- Destination IP
- Source IP/CIDR
- Priority (rule order)
- Destination port or port range
- TCP flags
- Protocol (ICMP, TCP, UDP, GRE)
- Actions
  - Accept (pass packets using only RFC protocol header validation)
  - Filter (only pass packets which pass the selected filter or the default filter based on port ranges)
  - Drop (block all packets matching this rule)

## Filter Profiles
We currently provide the following filter filters:
- Minecraft Java (TCP)
- HTTP (TCP)
- TLS (TCP)
- RDP (TCP)
- SSH (TCP)
- RakNet (Rust, MCPE, Terraria, 7 Days to Die, ...) (UDP)
- Source Engine Gold/1/2 (UDP)
- Steam Query (UDP)
- Plasmo Voice Mod (UDP)
- DayZ (UDP)
- TeamSpeak 3/5 (UDP)
- WireGuard (UDP)
- QUIC (UDP)
- FiveM (TCP/UDP)

In addition to these filters we provide generic and stateful protection for the following protocols:
- TCP
- UDP
- ICMP
- GRE/IPIP, ...

## Mitigation settings

In addition to our firewall you can set different mitigation thresholds for each of your
protected IPs.
Currently, we offer the following thresholds/settings through our panel:

- SYN threshold (Indicates when SYN rate-limits should take place or as of when you consider it an attack)
- Minecraft threshold (To allow pingers or server lists to properly reach your server, set this to a moderate value)
- Fragment threshold (This value should be set with your hosted services in mind, if or if not they are using fragments)
- AMP threshold (This threshold may be set low if you do not encounter issues when reaching services mostly used for AMP attacks)
- UDP threshold (The threshold for anomaly based udp attack detection, only used if no filter is applied)
- ACK threshold (TCP ACK anomaly detection that is only used when no actual application filter for that TCP port is set)
- Attack duration (Specify how many seconds the filter should stay active after an attack. We recommend a value of a few minutes)
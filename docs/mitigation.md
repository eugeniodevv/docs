---
sidebar_position: 2
slug: /mitigation
title: "DDoS Mitigation"
---

# DDoS Mitigation

Our DDoS mitigation system consists of multiple stages to filter all kinds of DDoS attacks,
ranging from simple Layer 3/4 attacks to complex Layer 7 attacks.

## Anycasting

We operate multiple PoPs (points of presence) around the world, which can be found
[here](locations.md).
If an attack is launched against our network it will get distributed across all of our PoPs,
depending on where the attack is launched from.

This allows us to combine the power of all our scrubbing nodes to handle terabit scale attacks
without any downtime.

Another benefit of this approach are lower latencies, since all users are connected with our
closest PoP automatically.

## Volumetric Protection

We have deployed rules at the core switches of our Upstream provider ([Datacamp](https://www.datacamp.co.uk)).
That allows us to drop large scale volumetric attacks, like amplification & reflection, before reaching our
own scrubbing nodes.

Additionally, all of our subnets are protected by their own proprietary anti-DDoS solution
to handle more sophisticated Layer 3/4 attacks.

These rules alone can drop attacks of up to **130 Tbit/s** on the edge.

### Common blocked L3/L4 attacks
- UDP floods of any kind
- TCP SYN ACK Reflection Floods
- ICMP Echo Request Floods
- IP Packet Fragment Attacks
- IGMP Floods
- TCP SYN Floods
- TCP Spoofed SYN Floods
- TCP ACK Floods
- TCP Fragmented Attacks

## Layer 7 Protection

Our Layer 7 Protection is always active and works in-line with zero TTM (time to mitigate).
All scrubbing nodes are connected with redundant high-bandwidth ports (n x 40G).

Every incoming packet is checked to make sure that it follows a specific application protocol,
like the [Minecraft Protocol](https://wiki.vg/Protocol).
These checks guarantee that only legitimate packets will be forwarded to your server
and any bad or invalid packet will be blocked at our edge.

Furthermore, we provide detailed logging and reporting capabilities,
allowing you to monitor your server's traffic and detect any unusual activity.
This information helps you to take appropriate action and further enhance your server's security posture.

All of our nodes are equipped with [eBPF XDP](https://en.wikipedia.org/wiki/Express_Data_Path) filters
to drop large attacks with even **millions of packets per second**.
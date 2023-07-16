# DDoS Mitigation

## Layer 4 Protection

We do protect our users against all kinds of Layer 4 attacks.
This protection sits at the first layer of our protection system and is capable of filtering up
to **30 Tbit/s** of dirty traffic.
You can get more detailed information here: [How the protection works](how_it_works.md)

When the attack is global, the mitigation services, replicated in eight OVH data centers across
three continents, activate simultaneously to combine their power and absorb the traffic.

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

Our Layer 7 Protection checks every incoming packet and makes sure that it is
following the [Minecraft Protocol](https://wiki.vg/Protocol).
This check guarantees that only legitimate Minecraft packets will be forwarded to your server
and any bad/invalid packet will be blocked at our edge.

Furthermore, we provide detailed logging and reporting capabilities,
allowing you to monitor your server's traffic and detect any unusual activity.
This information helps you to take appropriate action and further enhance your server's security posture.

All of our nodes are equipped with [eBPF XDP](https://en.wikipedia.org/wiki/Express_Data_Path) filters to drop attacks with even **millions of packets per second**.

We also use smart rate limits to avoid your server from getting overwhelmed by too many packets at once.

### Compatibility

Our service is compatible with any Java/Bedrock Minecraft game client,
as long as it follows the [Minecraft Protocol](https://wiki.vg/Protocol).

Note that anything you do in-game does not affect our proxy at all.

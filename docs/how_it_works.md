---
sidebar_position: 1
title: How it works
---

# How it works

NeoProtect is a highly available reverse proxy, sitting between your users and your server(s).

The setup is very quick as you only need to point your domains to our service through the [Panel](https://panel.neoprotect.net).
After that the traffic is routed through our service and only legitimate packets will be forwarded to your server.
Your server is now protected against all kinds of Layer 3/4 and Layer 7 attacks.

Keep in mind that you must  not expose your server's ip as that will allow attackers to target your server directly and not through our service.

We protect your server with an advanced technology based on two layers of mitigation software.
Both layers provide a **permanent mitigation** to keep your server online at all times.
New attacks are analyzed automatically in order to improve our filters.

## How does the protection work?

### The first layer (L3/L4)

NeoProtect has the majority of their servers hosted at [OVH](https://www.ovhcloud.com), which are
famous for their fabulous in built DDoS protection.

In this layer all Layer 3-4 attacks are filtered at the edge of OVH and are unable to reach your servers.

The only problem is, they do not protect against Layer 7 attacks, targeting Minecraft servers,
like bot attacks. That's why we implemented a second layer, the traffic has to pass through.

### The second layer (L7)

In the second layer we perform application level (Layer 7) filtering in accordance with
the [Minecraft Protocol](https://wiki.vg/Protocol_FAQ#What.27s_the_normal_login_sequence_for_a_client.3F),
which is helping us to mitigate all kinds of bot and flooding attacks.

We also use Deep Packet Inspection (DPI) to strictly authenticate each packet against the Minecraft Protocol
to make sure that no invalid packets can reach your backend servers.

Additionally, we use more advanced checks to ensure that the majority of the attacks won't reach your server.

---
sidebar_position: 5
---

# Latency / Stability issues

If you observe any ping related issues it is very important to **not just open a ticket and say
"My ping is high, fix it!"** but to **provide useful information** for us to trace the problem.

## Rules before we investigate

We need **at least 3 players** of your server that have similar issues before we investigate.
All of these players need to provide a traceroute and/or other information.

## How to gather information

### Via a Traceroute

A traceroute helps to identify weak spots in your route over the internet.

#### Tutorial:

1. Open your command line (CMD)
2. Enter the following command:
   - Windows: `tracert anycast.neoprotect.ovh`
   - Linux/Mac: `traceroute anycast.neoprotect.ovh`
3. Wait until it finishes to print hops (can take a bit longer on windows)
4. Send a screenshot of that into your ticket

Note that this needs to be done by the players having these issues.

---
sidebar_position: 9
title: "Ping/stability issues"
---

# Ping/stability issues

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

### Via our built-in debug tool

This helps us to identify at which tcp connection the problem lies.

The typical proxying structure would look like this:

_Player_ -> _NeoProtect_ -> _BungeeCord/Velocity/Any other proxy_ -> _Spigot_

Anywhere in on of these "arrows" displaying a tcp connection, could be an issue.
With this method we are able to locate where the issue lies.

#### Tutorial:

To use that you need to [download our plugin](../features/neoplugin.md#install-instructions) and have it setup correctly.

After that you are able to use the command `/np debugTool` to start the debug.
It will run and once its finished, you will get a path where you can find the gathered information.

Send that into your ticket and we will analyse it for you.
---
sidebar_position: 9
title: "'Server is offline' error"
---

# Resolving the 'Server is offline' error

This error indicates that something is wrong when our nodes try to reach your backend.
While we do provide assistance with resolving this, this site should be self-explanatory and should
help you to resolve these issues completely.

## Checklist:

### 1. Check proxy protocol

Here we need to differ between two cases:

#### You use our plugin

To make sure your settings are properly working, activate proxy protocol in the plugin configuration
(**do not touch it in the panel**) and restart your server. This should fix any proxy protocol issue as
long as the plugin has the right api key.

#### You do not use our plugin

Make sure to have set ALL config options we listed [here](../features/proxy_protocol.md) and to have proxy protocol
turned on in our panel.

### 2. Check if you entered the right backend ip:port

Just re-check if this was the right backend ip and port you connected with before.

_You might use the command `ss -tulpn` on linux servers to see if the port is open on your machine._

### 3. Check your firewall for firewalled ports

You most likely know how to do that as you must have set it up in advance.

Here are a few commands to help you check your linux firewall:

- `ufw status`
- `iptables -S`
- `iptables -t raw -S`

### 4. Check for other interfering plugins

Please check if you have any plugins still installed from other protection provider you may were previously.

Also: You might want to check if any antibot blocks connections or rate limits them. (That can also be caused by bungee forks)


### 5. Check for your hosters protection

There are a few hosters out there that have their own ddos protection and they cause issues due to 
blocking traffic coming from neo.

This is as all your traffic comes from only a few IPs (which would to them most likely appear suspicious)
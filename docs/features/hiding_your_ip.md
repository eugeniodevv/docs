# Hiding your server's IP

At all times, several devices are scanning the internet to identify open ports and gather data about them.
These systems might expose your backend's IP address, which could leave your network open to direct attacks that could potentially bypass NeoProtect's mitigation measures entirely.

Therefore, it's highly important to **only allow connections to your Minecraft server port from our edge IP addresses**. You can use any firewall solution to achieve this, e.g. IP-tables/UFW or even hoster-level firewalls from Hetzner, OVH, etc.

You can find our current IP addresses through our [RESTful API](rest_api.md):

- as JSON: https://api.neoprotect.net/v2/public/servers
- as TXT: https://api.neoprotect.net/v2/public/servers/txt

In the event of an attack, which targets your server ip directly, you should check for any ip leaks on your end,
e.g. in your DNS records (see [DNS setup](../setup/dns.md)), or a missing firewall.
After the leak is fixed you must get a new server IP from your hoster,
which can be requested through their support.

If you need further help, e.g. to set up the firewall rules on your server,
don't hesitate to contact our [Support](../support.md).
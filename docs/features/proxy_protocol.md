# Proxy Protocol (ip forwarding)

[Proxy Protocol](https://www.haproxy.org/download/1.8/doc/proxy-protocol.txt) is a standardized protocol,
which allows your backend server to receive the **real ip addresses** of your users.

:::caution

Disabling Proxy Protocol can cause many problems with your backend server, e.g., ip banning.

That's why you should **always enable Proxy Protocol**.

:::

## How to enable proxy protocol correctly

1. Visit the **Backends** section on our [Panel](https://panel.neoprotect.net).
2. Enable "Proxy Protocol"
3. Configure your backend server (see below)
4. Restart your server to apply the config changes

### BungeeCord / Waterfall

Open `config.yml` and set:

```yaml
proxy_protocol: true
```

### Velocity

Open `velocity.toml` and set:

```toml
haproxy-protocol = true
```

### Paper 1.19+

Only enable it if you are not running a proxy like BungeeCord/Velocity in front of your server.

Since version 1.19 Paper supports Proxy Protocol natively and doesn't require any plugin.

Just open `config/paper-global.yml` and set:

```yaml
proxy-protocol: true
```

### Bukkit / Spigot / Paper < 1.19

Only enable it if you are not running a proxy like BungeeCord/Velocity in front of your server.

If your server software doesn't support proxy protocol natively,
just install a plugin which implements the proxy protocol:

https://www.spigotmc.org/resources/haproxy-protocol-implementor.103193/

### Geyser

Open `config.yml` and set:

```yaml
enable-proxy-protocol: true
...
use-proxy-protocol: true
```

Don't hesitate to contact our [Support](support.md) if you have further questions.
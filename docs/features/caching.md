# Caching

Our system caches the status response (including MOTD & icon) of your backends and keeps
them in memory for a few seconds.
As soon as a user pings your server the status response is delivered directly from our edge,
reducing your backend load and latency. It also protects you against status request/ping floods,
which could harm your server.

Therefore, it's highly recommended to keep this setting enabled.

If you still want to disable or purge the cache completely it's possible through
our [Panel](https://panel.neoprotect.net) or our [Rest API](rest_api.md).

Note: We always cache the server status for each of your domains separately, which means that even
MOTD plugins with special behavior can work as expected.

## Why do I see "13.37.69.69 initial handler has pinged" in the console?

That's because our proxy periodically fetches the status (MOTD & icon) from your backend servers, to maintain the cache (see above).
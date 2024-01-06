---
sidebar_position: 9
---

# "Unknown host" error

This is a very common error displayed by the client indicating one of the following things:

1. The dns record you try to reach does not exist or was not properly configured
2. Your server is blocked by Mojang (Check [here](https://ismyserverblocked.com))
3. The dns record propagation did not yet reach the players dns
4. The dns server the player uses is somehow returning nothing (Or non-wanted things)

### Check if you configured the dns properly

You can verify our dns configuration by taking a look at our [setup tutorial page](../gameshield/setup.md)

### Check if your server is blocked by Mojang

You can take a look [here](https://ismyserverblocked.com) to check that. 

After that you might file an appeal at Mojang.

### For the other, player dns related problems

You might want to cooperate with the players and getting them to change their dns servers to
more reliable dns servers like cloudflare or google.

On windows, your player might execute `ipconfig /flushdns` as well to delete all cached dns answers.

# Load Balancing

Load balancing is a core networking solution used to distribute traffic across multiple servers.
This allows you to run multiple backend servers, like BungeeCord servers, and get your players automatically balanced
between all of them.
We offer multiple load-balancing algorithms for your backend servers, which provide different benefits.

## Supported Algorithms
- Random (connections are forwarded to a random backend server)
- Round Robin (connections are distributed across all your backends sequentially)
- Least Connections (connections are sent to the server with the fewest current connections/players)

## How it works
As soon as a player tries to connect to your server we order all of your backend servers
by the load balancing algorithm, which can be changed in our [Panel](https://panel.neoprotect.net).

After that, our system tries to connect the player to all the backends in sequence until a reachable backend is found.
If none of your backends are reachable the player will be disconnected with an offline message.
This message can be customized in our [Panel](https://panel.neoprotect.net).

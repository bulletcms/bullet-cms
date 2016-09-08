# bullet-cms
cms as fast as a bullet

Tech stack:
```
_________________________
Haproxy
(load-balancer+anti-ddos)-------
  |                            |
  v                            v
____________           ______________________
Varnish                Node Websockets Server
(http cache)           (SocketIO)
  |                     |       |
  v                     |       |
________________        |       |
Node API Server         |       |
(Koajs + React)-----    |       |
  |                |    |       |
  |                |    |       |
  |                v    v       |
  |               _______       |
  |               Redis         |
  |               (cache)       |
  |                             |
  v                             v
____________________________________________
database (Cassandra, Google Datastore, etc.)
```

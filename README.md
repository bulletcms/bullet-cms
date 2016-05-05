# bullet-cms
cms as fast as a bullet

Tech stack:
```
_________________________
Haproxy
(load-balancer+anti-ddos)-------
  |                            |
  v                            v
_______                ______________________
Varnish                Node Websockets Server
(cache)                (SocketIO)----------
  |                         |      |      |
  v                         |      v      |
__________________________  |    _____    |
Falcon Website API          |    Redis    |
(gunicorn+meinheld+celery)  |             v
  |     |     |             |         ________
  |     v     |             |         RabbitMQ
  |   _____   |             |
  |   Redis   |             |
  |           v             |
  |       ________          |
  |       RabbitMQ          |
  v                         v
____________________________________________
database (Cassandra, Google Datastore, etc.)
```

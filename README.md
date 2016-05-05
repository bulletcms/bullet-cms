# bullet-cms
cms as fast as a bullet

Tech stack:
```
__________________________
Haproxy
(load balancer+anti-ddos)-------
  |                            |
  v                            v
_______                _____________________
Varnish                Flask
(cache)                (meinheld-websockets)
  |                         |      |      |
  v                         |      v      |
__________________________  |    _____    |
Flask                       |    Redis    |
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

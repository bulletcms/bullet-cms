# bullet-cms
cms as fast as a bullet

Tech stack:
```
_________________________
Haproxy
(load balancer+anti-ddos)
  |                 |
  v                 v
_______           ________________________
Varnish           Flask
(cache)           (socketio/gevent-socket)
  |                    |      |        |
  v                    |      v        |
_________________      |    _____      |
Flask                  |    Redis      |
(gunicorn+celery)      |               v
  |     |     |        |           ________
  |     v     |        |           RabbitMQ
  |   _____   |        |
  |   Redis   |        |
  |           v        |
  |       ________     |
  |       RabbitMQ     |
  v                    v
____________________________________________
database (Cassandra, Google Datastore, etc.)
```

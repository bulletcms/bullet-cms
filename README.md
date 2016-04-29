# bullet-cms
cms as fast as a bullet

Tech stack:
```
_________________________
Haproxy
(load balancer+anti-ddos)
  |----------------
  |               |
  v               v
_______         ___________________
Varnish         Flask
(cache)         (socketio+RabbitMQ)
  |               |      |
  v               |      v
_______________   |    _____       
Flask             |    Redis
(http+RabbitMQ)   |
  |     |         |
  |     v         |
  |   _____       |
  |   Redis       |
  |               |
  v               v
____________________________________________
database (Cassandra, Google Datastore, etc.)
```

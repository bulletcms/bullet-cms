# bullet-cms
cms as fast as a bullet

Tech stack:
```
_______
Haproxy
  |----------------
  |               |
  v               v
_______         ___________________
Varnish         Flask
(1 min cache)   (socketio+RabbitMQ)
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

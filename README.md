# bullet-cms
cms as fast as a bullet

Tech stack:
_______
Haproxy
  |----------------
  |               |
  v               v
_______         ________________
Varnish         Flask (socketio)
  |               |--------------------------------
  |               |               |               |
  v               |               v               v
____________      |             _____           _______________
Flask (http)      |             Redis -------> Python RabbitMQ
  |               |                               |
  |               |                               |
  v               v                               v
____________________________________________________
database (Cassandra, Google Datastore, etc.)

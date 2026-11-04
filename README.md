# VideoGrace online pilot

Static web-client deployment for https://online.videograce.ru.

The command connection tries the trusted demo ingress routes. All routes use the
same demo server; this deployment is not an independent backend or a database replica.

REST/auth ingress: https://demo1.videograce.ru.
Command WebSocket routes: wss://demo.videograce.ru, wss://demo1.videograce.ru.

Only generated public client assets are published here. No server credentials,
private source repository, configuration secrets, or server databases are included.

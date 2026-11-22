# VideoGrace online pilot

Static web-client deployment for https://online.videograce.ru.

The command connection tries the trusted demo ingress routes. All routes use the
same demo server; this deployment is not an independent backend or a database replica.

REST ingress preference: demo.videograce.ru, demo1.videograce.ru, demo2.videograce.ru.
Persisted account identity remains demo1.videograce.ru.
Command WebSocket routes: wss://demo.videograce.ru, wss://demo1.videograce.ru, wss://demo2.videograce.ru.

Only generated public client assets are published here. No server credentials,
private source repository, configuration secrets, or server databases are included.

2026-11-22 hotfix: restore public PWA sessions through the primary REST ingress
without credentialed CORS when an explicit refresh token is available. Built from
VideoGrace 9e8bb5c63 plus the isolated ControlWS refresh fix; no experimental mesh UI
or server changes are included. Previous hashed assets are retained for open clients.

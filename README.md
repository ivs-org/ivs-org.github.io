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

2026-11-22 follow-up (VideoGrace 0c62146ef): explicit JSON 401 on refresh now
requests sign-in even when a legacy cookie marker remains. Preserve local chat
history and retry transient transport errors. Still built from 9e8bb5c63 with only
the ControlWS hotfixes. Entry: index-C9k8n-Rg.js.

2026-11-22 mesh pilot: publish the full VideoGrace T-177 web client at 0c62146ef,
including coordinator admin monitoring and both session recovery hotfixes. The demo
server now coordinates three mesh-capable RTC workers. Inter-node encryption is
not enabled in this temporary pilot; ingress is restricted to the RTC source IPs.

2026-11-23: publish VideoGrace 3.0.261123 (T-177, source 109a4cde9),
client protocol 619. Demo and all three required RTC media nodes now run the
same signed Linux release. Entry: index-wOBIphDC.js. Previous hashed assets
remain available for already open tabs.

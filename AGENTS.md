# Hinweise fuer Agenten

## Web-Oberflaechen: nie indexieren (Operator, 15.11.2026)

Jede Web-Oberflaeche, die dieses Repo auf einer VM oder einem Server betreibt, sendet `X-Robots-Tag: noindex, nofollow, noarchive, nosnippet`. Wo der Proxy es kann, liefert er zusaetzlich `/robots.txt` mit `Disallow: /`. Gesetzt wird das am Proxy vor der App (Pomerium, Caddy, Traefik, nginx), unabhaengig von der App, und ein Test im Repo haelt es fest. Hinter Pomerium (031) gilt der Header schon global. Neue Dienste bekommen das mit dem ersten Rollout. Ausnahme sind nur die oeffentlichen Webseiten 300, 301, 310 und 320.

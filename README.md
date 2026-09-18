# ToDo-Applikation mit Docker

Dieses Projekt ist eine einfache **ToDo-Applikation**, entwickelt mit [Node.js](https://nodejs.org) und [Express](https://expressjs.com). Sie dient als Übung im Rahmen zu Git, GitHub und Docker.

## Voraussetzungen

Bevor man startet, muss man sicher stellen , dass Folgendes auf dem Rechner installiert ist:

-   [Node.js](https://nodejs.org) (inkl. npm)
-   [Git](https://git-scm.com)
-   [Docker](https://www.docker.com)

## Repository klonen

Danach sollte man das Repository mit folgendem Befehl auf deinen Computer:

bash
git clone https://github.com/DEIN-USERNAME/docker-nodejs-sample.git

Wechsle anschliessend in das Projektverzeichnis:

```bash
cd docker-nodejs-sample
```

## Pakete installieren

Installiere alle benötigten Node.js-Abhängigkeiten mit:

```bash
npm install
```

## Anwendung lokal starten

Starte die Anwendung im Entwicklungsmodus mit:

```bash
npm run dev
```

Die Anwendung ist danach unter folgender Adresse erreichbar:

```
http://localhost:3000
```

## Docker-Image erstellen

Erstelle ein Docker-Image der Anwendung mit:

```bash
docker build -t docker-nodejs-sample .
```

## Anwendung mit Docker starten

Starte einen Container basierend auf dem erstellten Image:

```bash
docker run -p 3000:3000 -d docker-nodejs-sample
```

Die Anwendung ist danach ebenfalls unter `http://localhost:3000` erreichbar.

## Anwendung mit Docker Compose starten

Alternativ kann die Anwendung mit **Docker Compose** gestartet werden:

```bash
docker compose up -d
```

## Anwendung stoppen

Um den Container zu stoppen, der über `docker run` gestartet wurde:

1. Container-ID ermitteln:

```bash
   docker ps
```

2. Container stoppen:

```bash
   docker stop CONTAINER_ID
```

Falls die Anwendung mit **Docker Compose** gestartet wurde, genügt:

```bash
docker compose down
```

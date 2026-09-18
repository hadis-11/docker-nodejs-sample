# ToDo-Applikation mit Docker

Dieses Projekt ist eine einfache **ToDo-Applikation**, entwickelt mit [Node.js](https://nodejs.org) und [Express](https://expressjs.com). Sie dient als Übung im Rahmen zu Git, GitHub und Docker.

## Voraussetzungen

Bevor man startet, muss man sicher stellen , dass Folgendes auf dem Rechner installiert ist:

-   [Node.js](https://nodejs.org) (inkl. npm)
-   [Git](https://git-scm.com)
-   [Docker](https://www.docker.com)

## Repository klonen

Danach sollte man das Repository mit folgendem Befehl auf dem Computer herunterladen:

bash
git clone https://github.com/DEIN-USERNAME/docker-nodejs-sample.git

Anschliessend in das Projektverzeichnis wechseln:

```bash
cd docker-nodejs-sample
```

## Pakete installieren

Installiere alle benötigten Node.js-Abhängigkeiten mit:

```bash
npm install
```

## Anwendung lokal starten

Den Befehl in der Entwicklungsumgebung (z.B Visual studio code) ausführen mit:

```bash
npm run dev
```

Die Anwendung ist unter folgender Adresse erreichbar:

```
http://localhost:3000
```

## Docker-Image erstellen

Das Docker-Image erstellen mit:

```bash
docker build -t docker-nodejs-sample .
```

## Anwendung mit Docker starten

den Container starten basierend auf dem erstellten Image:

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

1. Container-ID herausfinden:

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

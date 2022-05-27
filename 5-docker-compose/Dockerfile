# Das Image auf dem der Container basieren soll
FROM node:slim
# Das Verzeichnis mit dem das Dockerfile weiter arbeiten soll
WORKDIR /app
# Kopiert alle Daten vom aktuellen Ordner im Hostsystem in den aktuellen Ordner im Image (/app)
COPY . .
# RUN führt Befehler zu zur Buildzeit aus
RUN echo "Ich werde zur Buildzeit ausgefuehrt"
# Startbefehl für den Ausführungszeitpunk (beendet der Befehl, beendet der Container)
ENTRYPOINT ["node", "index.js"] 
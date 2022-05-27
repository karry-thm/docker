[Zurück](../README.md)

# 2 Container starten

Es gibt mehrere Wege container zu starten. Im einfach lokalen Kontext bietet sich der ```docker run ...``` Befehl am besten an. Alternativen sind Services oder das Starten über ```docker compose```.

## 2.1 Hello World-Container

Docker probiert das Image zu downloaden (immer wenn ein Container mit lokal nicht vorhandenem) und startet es.

```docker run hello-world```

## 2.2 Node-Red

### 2.2.1 Starten

Startet den Container und macht ihn auf dem Port 1880 (vor dem Doppelpunkt ist Hostsystem nach dem Doppelpunkt im Container). ```-d``` gibt an das der Prozess detached laufen soll - also im Hintergrund und nicht an die Lebenszeit des Befehls gebunden.

```docker run -it -p 1880:1880 --name nodered -d nodered/node-red```

### 2.2.2 Konsolenausgabe betrachten

Gibt die Konsolenausgabe aus, bis der Prozess mit ```STRG+C``` beendet wird. Ohne ```-f``` wird die aktuelle Konsolenausgabe ausgegeben und man erhält den Prompt zurück.

```docker logs -f nodered```

### 2.2.3 Stoppen

Der Befehl stoppt den Container anhand des Namens, den wir vorher vergeben haben.

```docker container stop nodered```
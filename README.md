# Digitale Erde

Ein interaktiver 3D-Globus, der sich von der globalen Perspektive bis zu OpenStreetMap-Straßendaten zoomen lässt.

## Starten

Die Anwendung ist eine statische Website ohne Build-Schritt. `index.html` über einen lokalen Webserver bereitstellen, beispielsweise:

```powershell
python -m http.server 8080
```

Danach `http://localhost:8080` im Browser aufrufen.

## Funktionen

- frei dreh- und neigbarer 3D-Globus
- Zoom vom Orbit bis zu Straßenebene
- OpenStreetMap-Kartendaten bis Zoomstufe 19
- responsive Bedienung für Maus und Touch
- kompakte Zoom-, Home- und Höhenanzeige

## Datenquellen

Die Kartenkacheln stammen von [OpenStreetMap](https://www.openstreetmap.org/copyright). Für öffentlich stark frequentierte Deployments sollte ein geeigneter Tile-Provider entsprechend der OSM-Tile-Usage-Policy verwendet werden.

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
- Orthofoto als Standardebene (Esri World Imagery, Zoomstufe 19)
- OpenStreetMap-Kartendaten bis Zoomstufe 19
- umschaltbare Orthofoto-Ebene mit sichtbarer Quellenangabe
- responsive Bedienung für Maus und Touch
- kompakte Zoom-, Home- und Höhenanzeige

## Verfügbarkeit der Kartenebenen

- Die Orthofotos werden über einen öffentlichen, tokenfreien Esri-World-Imagery-Endpunkt bezogen.
- OpenStreetMap bleibt gleichzeitig als Straßen-Basis aktiv. Wenn innerhalb von 15 Sekunden mindestens vier Orthofoto-Kacheln nicht geladen werden können, blendet die Anwendung die Orthofotos aus und zeigt automatisch die Straßenkarte.
- Damit die Kartenkacheln geladen werden können, benötigt der Browser eine Internetverbindung. Eine absolute Verfügbarkeitsgarantie für externe Kartenkacheln ist technisch nicht möglich; dafür wäre ein eigener Tile-Cache/CDN oder ein Anbieter mit SLA erforderlich.

## Datenquellen

Die Orthofotos stammen aus [Esri World Imagery](https://www.esri.com/en-us/arcgis/products/arcgis-living-atlas/basemap) (Quellen: Esri, Maxar, Earthstar Geographics und GIS User Community). Die Straßenkarte stammt von [OpenStreetMap](https://www.openstreetmap.org/copyright). Für öffentlich stark frequentierte Deployments sollte ein geeigneter Tile-Provider entsprechend der OSM-Tile-Usage-Policy verwendet werden.

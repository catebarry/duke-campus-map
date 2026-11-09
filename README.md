# Duke Campus Path Finder

Find the shortest walking route between Duke campus buildings, with a separate **accessible route** that avoids stairs and inaccessible connections.

**Live demo:** https://catebarry.github.io/duke-campus-map/

## How it works
- Campus buildings are nodes in a weighted graph; walkways are edges with a default walking time and (where the path is step-free) an accessible walking time.
- Routes are found with Dijkstra's algorithm, once per route type.
- The map uses [Leaflet](https://leafletjs.com) with [OpenStreetMap](https://www.openstreetmap.org/copyright) data.

## Run locally
Open the page through a local server (browsers don't send a Referer from `file://`, which OpenStreetMap's tile policy requires):

```
python3 -m http.server 8000
```
Then visit http://localhost:8000

## Repo layout
- `index.html` – the web app (deployed with GitHub Pages)
- `desktop/` – original Python (Tkinter + folium) version

Originally built as a group project for CS 232 at Duke.

Map data © OpenStreetMap contributors.

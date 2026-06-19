Slovenian museums Mapbox starter
=================================

Files needed
------------
1. index.html
2. data/museums.csv
3. Internet access for Mapbox GL JS and Papa Parse CDN
4. A Mapbox public access token

Recommended folder structure
----------------------------
slovenian-museums-map/
  index.html
  data/
    museums.csv

Important
---------
Do not load the CSV from:
C:\Users\ukanjir\ZRC SAZU Dropbox\ursa kanjir\FF_Storymap\Vzhodnoazijski predmeti in zbirke v Sloveniji.csv

Browsers usually cannot fetch a local Windows path from JavaScript. Copy or export the CSV into the data folder and rename it to museums.csv.

Run locally
-----------
From the slovenian-museums-map folder:

python -m http.server 8000

Then open:

http://localhost:8000

CSV requirements
----------------
The CSV must have:
- one museum or collection record per row
- WGS84 latitude in decimal degrees
- WGS84 longitude in decimal degrees
- a museum/institution name column

The HTML tries to detect common Slovenian and English column names. If your CSV uses different headers, edit FIELD_CANDIDATES near the top of index.html.

Popup content
-------------
Edit POPUP_FIELDS in index.html to choose which table columns appear in the popup.

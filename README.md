### Map of Toronto's Red Light Cameras

This is a simple web-map showing the location of Toronto's Red Light Cameras

It is live here: http://jamaps.github.io/red_light_cameras_toronto/

- Data is from the City of Toronto Open Data and OpenStreetMap.  
- The map tiles are from Mapbox.  
- And the map was built using leaflet.js library.

#### This was how I built the map:

1 - Pull the data off the City of Toronto's Open Data website.

2 - Import the data as a shapefile into QGIS and inspect.

3 - In the attribute table, concatenate the two string road fields into one like this:

    ROADS_1 || " & " || ROADS_2

4 - Remove unneeded fields and export as a .geojson file

5 - Build the map in index.html using the documentation from leaflet.js

6 - Link to a set of map tiles from MapBox and load into the map with L.tileLayer.

7 - Save the .geojson file as a .js file and edit it so the data is attached to a variable

    var campoints = { geojson_data }

8 - Create map icon for camera locations and load it into the map with the .js file using L.geoJson

9 - Set the bounds of the map and add a title to the map.

10 - Add attribution as a separate div at the bottom of the map.

11 - Use CSS to style and fit both divs into a single page view without a scroll bar

    #map { height: calc(100vh - 17px); }
    #footer { height: 16px; }

That's about it.

Feel free to email me with any comments or questions at jeff.allen |at| mail.utoronto.ca

Jeff Allen

This map and its code is CC-BY-CA 3.0



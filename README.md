# oi-risk-vis
Risk analysis visualisation tool

https://www.mapbox.com/mapbox-gl-js/style-spec/
Maputnik for developing syles

# Prepare data
Download the ``boundaries`` and ``network`` data

Unzip in ``/incoming_data`` folder

    unzip ~/Downloads/boundaries.zip -d incoming_data/
    unzip ~/Downloads/network.zip -d incoming_data/

Convert the incoming shapefiles into a *.mbtiles file

    ./convert.sh

# Run the Tile server

Start the docker contrainer

    docker run -it -v $(pwd):/data -p 8080:80 klokantech/tileserver-gl --config config.json

Open the webbrowser to view the Tile Server

    firefox http://localhost:8080/

# Run the App

Install required packages

    npm install

Start app

    npm start

This should automatically start the browser, if not

    firefox http://localhost:3000/
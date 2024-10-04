
# Deploy the Citi Bike Project

In this activity, we used the Citi Bike API to get the status and location of every Citi Bike station in New York City.

## Project

We used the [Citi Bike station information endpoint](https://gbfs.citibikenyc.com/gbfs/en/station_information.json) to get information about the station names and locations.

Note the following details:

* Each object in the `stations` array has `station_id`, `name`, `capacity`, `lat`, and `lon` properties.
* The [logic.js](Unsolved/static/js/logic.js) file contains coordinates that you can use to position a Leaflet map over New York City.

We created a function named `createMap` that takes `bikeStations` as an argument. This function created both the tile layer and an overlay with the pins for each station.

We created a second function named `createMarkers` that took `response` as an argument.

* Used the response from a future D3 call, looped through the stations, and then created a marker to represent each station.
* Gave each marker a popup to display the name and capacity of its station.

In the `createMarkers` function, we passed the resulting bike markers to the `createmap` function as a `layerGroup`.

We used D3, retrieve JSON data from the [Citi Bike station information endpoint](https://gbfs.citibikenyc.com/gbfs/en/station_information.json), and then call the `createMarkers` function.

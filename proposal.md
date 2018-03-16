# Project Proposal: CAPSTONES

---

## Project Description

Open-Nodes: Weather 
- this is the opensource, communty-maintained, data gathering and data visualing tool. 

(Open-Nodes: Water)

## Problem statement
Access to data in realiable, useable ways provides insights not realized in the past. IoT technologies offers unique oppertunities to capture higher resolution, fast, cheaper from more points and capture more variables with relative ease. 

Agribusiness, raw materials, rural areas, and developing economies all area heavily effected by water scarcity, weather and access to high quality data for making business decisions and strategizing how to best accomplish their goals. 

By establishing a ground-based data collection device whose collection capabilities are modular, inexpensive, and deliver data in a easily digestible format for public and private data consumption.

(Fresh water scarcity is projected to be one of the biggest problems the planet will deal with as climate change continues - monitoring and providing the public tools to empirically assess their resource is vital.)

## How will your project solve this problem?
Raspberry Pi mounted with temperature, humidity, barometric pressure, solar panel (cloud cover?), and any other sensing pieces I can afford to throw on there.

The Pi will be configured to post data to a server using WiFi or Bluetooth. The server will store data in a database, updating regularly, and do some formatting/repackaging of the data to prep it for the client.

The client will be a React + Gatsby SPA that allows users to view real-time data collection results and historical data collection trends in a slick visualization using C3 or Chart.js. 

Beyond data from a single point - the utility comes from many data points. Along a pipeline, riverway, transit area, national park, places with sensitive microclimates, etc.

## Map the user experience
1. Users will visit the site and be met with a visual experience of the current weather topics pulled from media outlets.
2. Users will have the option to view a map all the collection points and select other points to see the current data. 
3. Users can view historical data as charts, graphs and overlay with data from other opensource providers (Wunderground, NOAA, etc).
4. Users will be prompted to buy a collection device and maintain it, connect it to their own wifi and increase the resolution of the community weather (water) collection array.


## What technologies do you plan to use?
- HTML, CSS, JavaScript
- React (+ Redux), Gatsby: SPA, SWA, continuous deployment/integration strategy (to incorporate GraphQL)
- APIs: build my own for sensor data --> express server, leaflet/mapbox
  - (Stretch goals: Wundergraound, NOAA, Planet OS?)
  - Stretch Goals: social auth + stripe for people to buy their own pi data collector
- Node.js, Express.js, Knex.js, PostgresSQL
- Sockets.io for file transfer/datadumps
- Raspberry Pi (debian) + sensors + wifi card

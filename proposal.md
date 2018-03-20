# Project Proposal: CAPSTONES

---

## Project Description

ClimaStatus 
- a DIY for your home climate monitoring. Indoor, outdoor, join friends, etc.
- For MVP: 
    - build the data server to catch the posting data from the Pi. 
    - build the pi sensor
    - build the slick client side to show the data and let users configure their view (no OAuth for MVP)

## Problem statement

Access to data in realiable, useable ways provides valuble insights. IoT technologies offer unique oppertunities to capture higher resolution, fast, cheaper from more points and capture more variables with relative ease. 

Agribusiness, raw materials, rural areas, and developing economies all are heavily effected by water scarcity, weather and access to high quality data for making business decisions and strategizing how to best accomplish their goals. 

By establishing a ground-based data collection device whose collection capabilities are modular, inexpensive, and deliver data in a easily digestible format for public and private data consumption users will be able to change behavior and act on new information previously not avaliable.

(HydroStatus: 
Fresh water scarcity is projected to be one of the biggest problems the planet will deal with as climate change continues - monitoring and providing the public tools to empirically assess their resource is vital. Expanding upon a weather node, a water quality assessment tool for the public or for stakeholders/resource managers will enable conservation actions to be taken quicker.)

## How will your project solve this problem?

Raspberry Pi mounted with temperature, humidity, barometric pressure, solar panel (relative cloud cover), and any other sensing pieces I can afford to mount on a single board. For MVP: temp, humidity, solar

The Pi will be configured to post data to a server using WiFi or Bluetooth. The server will store data in a database, updating regularly, and do some formatting/repackaging of the data to prep it for the client.

The client will be a React + Gatsby SPA that allows users to view real-time data collection results and historical data collection trends in a slick visualization using C3 or Chart.js. 

## Map the user experience

1. Users will have the option to view a map of all the collection points and select other points to see the current data. 
1. Users can view historical data as charts, graphs and overlay with data from other opensource providers (Wunderground, NOAA, etc).

## What technologies do you plan to use?

#### Front End
- HTML, CSS, JavaScript
- React (+ Redux), Gatsby: SPA, SWA, continuous deployment/integration strategy (to incorporate GraphQL)
- APIs: build my own for sensor data, leaflet/mapbox
  
#### Server
- Node.js, Express.js, Knex.js, PostgresSQL
- Sockets.io for file transfer/datadumps
- Raspberry Pi (debian) + sensors + wifi card


## STRETCH
(HydroStatus) - this is an entirely different project, really.

1. Build a couple Pi Sensors: 
    - Beyond data from a single point (the utility comes from many data points). 
    - Place a second build 'in the wild': 
        - Along a pipeline
        - riverway
        - transit area 
        - national park
        - places with sensitive microclimates, etc.
        - a map of data will be visually available to contextualize collection from a single point.

### User Stories
  - Stretch Goals: Wundergraound, NOAA, Planet OS? --> Addition data vis integrations or posting to public data orgs.
  - Stretch Goals: social auth + stripe for people to buy their own pi data collector

#### Strech Stories
1. Users will be prompted to buy a collection device and maintain it, connect it to their own wifi and increase the resolution of the community weather (water) collection array.
  - As a user I will be able to log in to see my personal data.
1. As a homeowner, I will be able to log in and see the data from my 'personal' device.
1. As a citizen, I will be able to see the data from other ClimaStatus units if I choose to share my data.
1. Users will visit the site and be met with a visual experience of the current weather topics pulled from media outlets.

  
 
#### References
- [Oracle Sense HAT station + John Wargs Weather Station](https://github.com/lebeerman/pi_weather_station)
- [Pi Component Listings](https://tutorials-raspberrypi.com/raspberry-pi-sensors-overview-50-important-components/)
- [kombucha thermostat on chip](https://learn.adafruit.com/kombucha-thermostat-with-circuitpython-and-feather?view=all)
- [Featherwing Data Logger Chip](https://learn.adafruit.com/adafruit-adalogger-featherwing?view=all)
- [Weather Station Info](https://www.raspberrypi.org/education/weather-station/)
- [Weather Pi Data Center](https://www.raspberryweather.com/)

# Airly

This app adds sensors with data from Airly via MQTT Discovery to the [Home Assistant](https://home-assistant.io/).

This is [AppDaemon](appdaemon.readthedocs.io/) app.

You can install this app via [HACS](https://custom-components.github.io/hacs/) or just download `airly.py` file and save it in `/config/apps` folder.

Go to [HA community](https://community.home-assistant.io/t/airly-integration-appdaemon/101455) for support and help.

- airly_apikey - Airly API key, string (required)
 - latitude     - latitude, float (required)
 - longitude    - longitude, float (required)
 - retain       - retain true or false for MQTT, boolean, default false (optional)
 - interval     - update interval, integer, default 5 min. (optional)
 - sensors      - dictionary of sensors to add, default pm1, pm25, pm10, caqi
                  (optional), available sensors: pm1, pm25, pm10, caqi,
                  temperature, humidity, pressure

## Configuration example
```yaml
airly:
  module: airly
  class: Airly
  airly_apikey: 12345678910
  latitude: 52.2323788
  longitude: 21.0439212
  retain: false
  interval: 10
  sensors:
    - pm1
    - pm25
    - pm10
    - caqi
    - temperature
    - humidity
    - pressure
```

## App arguments
key | optional | type | default | description
-- | -- | -- | -- | --
`airly_apikey` | False | string | | Airly API key
`latitude` | False | float | | latitude
`longitude` | False | float | | longitude
`retain` | True | boolean | `false` | retain `true` or `false` for MQTT
`interval` | True | integer | 5 | update interval [min]
`sensors` | True | dictionary | `[pm1, pm25, pm10, caqi]` | dictionary of sensors to add, available sensors: `pm1`, `pm25`, `pm10`, `caqi`, `temperature`, `humidity`, `pressure`

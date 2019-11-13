# This app is deprecated. Use [Airly custom component](https://github.com/bieniu/ha-airly) instead.

# Airly
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)
[![Buy me a coffee][buy-me-a-coffee]](https://www.buymeacoffee.com/QnLdxeaqO)

This app adds sensors with data from Airly via MQTT Discovery to the [Home Assistant](https://home-assistant.io/).

This is [AppDaemon](appdaemon.readthedocs.io/) app.

You can install this app via [HACS](https://custom-components.github.io/hacs/) or just download `airly.py` file and save it in `/config/apps` folder.

Go to [HA community](https://community.home-assistant.io/t/airly-integration-appdaemon/101455) for support and help.

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

[buy-me-a-coffee]: https://img.shields.io/static/v1.svg?label=%20&message=Buy%20me%20a%20coffee&color=6f4e37&logo=buy%20me%20a%20coffee&logoColor=white

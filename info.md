# This app is deprecated. Use [Airly custom component](https://github.com/bieniu/ha-ad-airly) instead.

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

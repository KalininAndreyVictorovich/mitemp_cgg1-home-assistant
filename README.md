# Home-Assistant sensor Xiaomi Mi Temperature and Humidity Sensor with Bleutooth LE and E-Ink display  

**WORK IN PROGRESS**

This library lets you read sensor data from a Xiaomi Mi Bluetooth LE Temperature and Humidity sensor.

## Functionality 
It supports reading the different measurements from the sensor
- temperature
- humidity

battery level and unit of measure are not supported yet.

## Installation
1. Copy `custom_components/mitemp_cgg1` directory into `custom_components` inside your HA directory 
(typically, where configuration.yaml is placed).
2. Add this block into `configuration.yaml`
    ```yaml
    sensor:
      - platform: mitemp_cgg1
        mac: '58:2D:34:xx:xx:xx'
        force_update: true
        cache_value: 60
        monitored_conditions:
          - temperature
          - humidity
    ```
    where `mac` property is Thermometer mac address. See [mitemp_bt docs](https://www.home-assistant.io/components/mitemp_bt/#configuration)
    for instructions.
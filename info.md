
[![hacs_badge](https://img.shields.io/badge/HACS-Default-green.svg)](https://github.com/custom-components/hacs)

# Passive BLE Monitor integration

![BLE_sensors](https://raw.githubusercontent.com/custom-components/ble_monitor/master/pictures/sensors.jpg)

This custom component for [Home Assistant](https://www.home-assistant.io) passively monitors [many different BLE devices](https://custom-components.github.io/ble_monitor/devices) of several different [brands](https://custom-components.github.io/ble_monitor/by_brand). BLE Monitor can also be used as device tracker for BLE devices with a static MAC address or with the UUID.


## More info

- [Documentation](https://custom-components.github.io/ble_monitor/#introduction)
- [Installation instructions](https://custom-components.github.io/ble_monitor/Installation)
- [Configuration](https://custom-components.github.io/ble_monitor/configuration_params)
- [Supported devices](https://custom-components.github.io/ble_monitor/devices)
- [Forward data from ESPhome](https://custom-components.github.io/ble_monitor/parse_data)
- [DIY sensors](https://custom-components.github.io/ble_monitor/bthome)
- [FAQ](https://custom-components.github.io/ble_monitor/faq)
- [New sensor request](https://custom-components.github.io/ble_monitor/sensor_request)
- [Developer documentation](https://custom-components.github.io/ble_monitor/developer_docs)
- [Forum](https://community.home-assistant.io/t/passive-ble-monitor-integration/)
- [Report issues](https://github.com/custom-components/ble_monitor/issues)

## Supported sensor brands

![BLE_sensors](https://raw.githubusercontent.com/custom-components/ble_monitor/master/pictures/sensors_2.png)

- Acconeer
- Air Mentor
- Amazfit
- ATC (custom firmware for Xiaomi/Qingping sensors)
- BlueMaestro
- Blustream (Taylor TaylorSense, D'Addario Humiditrak)
- BTHome
- b-parasite
- Ela
- Govee
- Grundfos
- HolyIOT
- Hörmann
- HHCC
- Inkbird
- iNode
- Jaalee
- Jinou
- Kegtron
- KKM
- Mikrotik
- Moat
- Oras
- Oral-B
- Qingping
- Relsib
- Ruuvitag
- Sensirion
- SensorPush
- Senssun
- SmartDry
- Switchbot
- Teltonika
- Thermobeacon (Thermoplus, Brifit, Oria)
- Thermopro
- Tilt
- Xiaogui (Scale)
- Xiaomi (MiBand)
- Xiaomi (MiBeacon sensors)
- Xiaomi (MiScale)


## Why isn't ESPHome Bluetooth Proxy not working with BLE monitor?

Please not that ESPHome Bluetooth Proxies cannot forward data to BLE monitor. Check out [this page](https://custom-components.github.io/ble_monitor/parse_data) for alternative solutions.

## Important announcement about the future of BLE monitor

Home Assistant 2022.8 has (improved) support for passive BLE devices directly in Home Assistant. For each brand, a core BLE integration will be developed, such that maintenance can be divided over more people, using the latest Bluetooth packages (bleak). I'm working together with the Home Assistant devs to move sensors from BLE Monitor to Home Assistant core integrations. During the transition, BLE monitor will still be available, but it is possible that the core HA Bluetooth integrations will not work niceley parallel to BLE monitor. **If it is not working together (common symptom is that core integrations stop updating after a while), try to enable active scan in the BLE monitor settings.** My advise, when all your sensors are available in Home Assistant, make the move. The aim is to have all sensors moved into Home Assistant as core integration. After the move, BLE monitor will probably be deprecated. If you want to help moving sensors from BLE monitor, feel free to help. Check out the links below.

**Some interesting links**

- Most pypi packages for the BLE parsing will be developed and collected here: https://github.com/Bluetooth-Devices

**Available as official HA integration**

The following integrations are available as official Home Assistant integration.
- BlueMaestro
- b-parasite (will be using BTHome with new firmware)
- BTHome
- Govee
- HHCC
- iBeacon
- Inkbird
- Kegtron
- Moat
- Oral-B
- Qingping
- RuuviTag
- SensorPush
- Sensirion (MyCO2 gadget)
- Thermobeacon (Thermoplus, Brifit, Oria)
- Thermopro / Sensorpro
- ThermoPlus
- Tilt
- Xiaomi (part 1 and 2)
- Device tracking based on MAC address (Bluetooth LE tracker integration)

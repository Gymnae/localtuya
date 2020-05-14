# python-tuya based home assistant custom component

This custom component uses the python-tuya fork that can talk with Tuya version 3.3

## Key extraction

- https://github.com/clach04/python-tuya/wiki has background information for how to get device id and local key.
(the device id can be seen in Jinvoo Smart App, under "Device Info").

- https://github.com/TuyaAPI/cli (tuya-cli list-app) have another technique using Tuya official app (works better on android)

### Instructions

Copy the folder localtuya into your home assistant custom_components folder (create the folder in the same place as your configuration.yaml lives

Set a config like so:

```
switch:
  - platform: localtuya
    host: 192.168.0.1
    local_key: 1234567891234567
    device_id: 12345678912345671234
    name: tuya_01
    protocol_version: 3.3
```
#### Notes : 

if your switch doesn't work (log error : "decrypt data must be aligned to block boundary in ECB mode") try with the previous protocol_version: 3.1

it's the case for switches NEO COOLCAM Wifi (https://www.szneo.com/en/products/show.php?id=229)

### Related Projects

  * https://github.com/sean6541/tuyaapi Python API to the web api
  * https://github.com/codetheweb/tuyapi node.js
  * https://github.com/Marcus-L/m4rcus.TuyaCore - .NET
  * https://github.com/SDNick484/rectec_status/ - RecTec pellet smokers control (with Alexa skill)

### Acknowledgements

  * Based on mytuya work (link missing)

# ESPHome CYD Lightswitch for Home Assistant

I used the examples [here](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display/tree/main/Examples/ESPHome) as a starting point to get two CYD (aka ESP32-2432S028R) displays to work in ESPHome.

## My setup:

### Page 1

#### Kitchen

- Kitchen cabinet LED lights controlled by Sonoff Basic R2 switches running tasmota grouped into one virtual switch
- Dining room sidelights controlled by a Gosund plug converted to tasmota
- Dishwasher monitored by a Gosund plug converted to tasmota
- Washing machine monitored by a Gosund plug converted to tasmota

### Garage

- Electric door "locked" via a Gosund plug connected via Tuya integration (refuses to be converted to tasmota)

### Page 2

#### Living Room

- Sidelights controlled by Sonoff Basic R2 switches running tasmota
- Door sensor connected via Tuya integration

#### Summer House

- Double lightswitch connected via Tuya integration:
  - Switch 1: interior lights
  - Switch 2: garden lights

***

In order for the yaml to work the following settings needed to be added to the secrets.yaml file:
 - kit_api_key
 - lroom_api_key
 - ota_password
 - wifi_ssid
 - wifi_password
 - ap_password

For some of the examples you need to copy font or image files to your ESPHome folder. Those
examples contains the instructions in the yaml file itself.

TODO

- Add details for HA side
- It would be nice to have one yaml file and change it programatically as both rooms share 445 of the 451 lines...
- Need to stop the switch from activating unless the backlight is on

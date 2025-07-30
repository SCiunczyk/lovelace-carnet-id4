Home-Assistant Lovelace card for carnet adapted to VW ID4


1. Download the images in the www folder and put them in /config/www

2. Put below content in your ui-lovelace.yaml

```yaml
title: VW ID4
path: id4
type: masonry
icon: mdi:car
cards:
  - elements:
      - entity: switch.id4_electric_climatisation
        image: /local/carnet/blank.png
        state_image:
          "on": /local/carnet/id4_heat.png
        style:
          left: 53.5%
          top: 29.5%
          width: 47%
        type: image
      - entity: switch.id4_charging
        image: /local/carnet/blank.png
        state_image:
          "on": /local/carnet/id4_light_charge.png
        style:
          left: 51.0%
          top: 74.5%
          width: 100%
        type: image
      - entity: binary_sensor.id4_parking_light
        image: /local/carnet/blank.png
        state_image:
          "on": /local/carnet/id4silver_light.png
        style:
          left: 30.0%
          top: 47.0%
          width: 60%
        type: image
      - entity: binary_sensor.id4_doors_locked
        image: /local/carnet/blank.png
        state_image:
          locked: /local/carnet/blink.gif
        style:
          left: 57%
          top: 42.3%
          width: 2%
        type: image
      - entity: binary_sensor.id4_doors_locked
        style:
          left: 47%
          top: 87%
        type: state-icon
      - entity: switch.id4_electric_climatisation
        hold_action: toggle
        style:
          left: 58%
          top: 87%
        type: state-icon
      - entity: switch.id4_charging
        style:
          left: 69%
          top: 87%
        type: state-icon
      - entity: sensor.id4_battery_level
        style:
          left: 78%
          top: 88%
        type: state-label
      - entity: sensor.id4_electric_range
        style:
          left: 91%
          top: 88%
        type: state-label
      - type: state-label
        style:
          left: 10%
          top: 10%
        entity: sensor.id4_charging_power
      - type: state-label
        style:
          left: 10%
          top: 20%
        entity: sensor.id4_charging_time_left
      - type: state-label
        style:
          left: 10%
          top: 30%
        entity: sensor.id4_charging_rate
    image: local/carnet/id4silver_light_off.png
    type: picture-elements
```

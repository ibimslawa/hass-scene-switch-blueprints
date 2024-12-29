# Scene Switch Automation Blueprints for Home Assistant (Tuya TS0044 & TS0043, Paulmann 501.34)
Since I use the Tuya scene switches in my smart home I wanted to use automation blueprints for them.
The 3 and 4 button scene switches have each a MQTT and action variant available.
Since Zigbee2Mqtt announced for their version 2.0 that the "_action" entities will be dropped, I wrote the MQTT blueprint variant which utilizes triggers on "action" MQTT topics for the desired devices.
However the "_action" entities will be still available and therefore I also added the action variants to this repo, which simply use an entity state trigger.
The Paulmann 50134 Wall Switch is also available as an blueprint.

## Available scene switch blueprints

**4-Button Scene Switch (Tuya TS0044 or alikes)**
Blueprint for simple 4 button scene switches. Original make is Tuya TS0044. Several white labels exist with different designs.
[Zigbee2Mqtt Docs: Tuya TS0042](https://www.zigbee2mqtt.io/devices/TS0044.html)

**3-Button Scene Switch (Tuya TS0043 or alikes)**
Blueprint for simple 3 button scene switches. Original make is Tuya TS0043. Several white labels exist with different designs.
[Zigbee2Mqtt Docs: Tuya TS0042](https://www.zigbee2mqtt.io/devices/TS0043.html)

**2-Button Scene Switch (Tuya TS0042 or alikes)**
Blueprint for simple 2 button scene switches. Original make is Tuya TS0042. Several white labels exist with different designs.
[Zigbee2Mqtt Docs: Tuya TS0042](https://www.zigbee2mqtt.io/devices/TS0042.html)

**Paulmann 501.34 Wall Switch**
Wall Switch with two groups each consisting of one on and one off button. 
[Zigbee2Mqtt Docs: Paulmann 501.34](https://www.zigbee2mqtt.io/devices/501.34.html)

**IKEA Single On/Off Switch (TRADFRI E1743)**
Scene switch from IKEA called "TRADFRI" with on and off button.
[Zigbee2Mqtt Docs: IKEA E1743 TRADFRI](https://www.zigbee2mqtt.io/devices/e1743.html)

## Blueprint variants

**Action Entity variant**
This variant utilizes a state trigger for an user-provided "_action" entity of the scene switch.
The "_action" entity is only available if "legacy_triggers" is activated in the configuration of Zigbee2Mqtt.
Edit this option directly in the GUI settings of Z2M or add this to your Z2M "configuration.yaml":
```
homeassistant:
  legacy_triggers: true
```

**MQTT variant**
This variant utilizes a MQTT topic trigger. 
For a user provided device name the blueprint is triggered on the "/action" topic.
Two slots are available for a device name.
The device name must be the one used in Zigbee2Mqtt and therefore in the MQTT messages.

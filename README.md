# Button Scene Switch Blueprints for Home Assistant utilizing MQTT triggers (Tuya TS004X)
Since the Zigbee2MQTT Add-on for Home Assistant will remove the "_action" and "_click" entities from Version 2.0 onwards, I sat myself down and updated the well-known blueprints for the Tuya TS004X scene switches and derived models.

The blueprints accepts one or two text inputs, which represent the device names in the MQTT publish topic send by Z2M to Home Assistant.
From Z2M simply put the name of the desired device into an automation with the blueprint and add sequences for the button presses.

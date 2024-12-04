# Button Scene Switch Blueprints for Home Assistant (Tuya TS004X)
Since the Zigbee2MQTT Add-on for Home Assistant will remove the "_action" and "_click" entities from Version 2.0 onwards, I sat myself down and updated the well-known blueprints for the Tuya TS004X scene switches and derived models.
The blueprints accepts one or two text inputs, which represent the device names in the MQTT publish topic send by Z2M to Home Assistant.
Simply from Z2M put the name of the desired device into an automation with a blueprint and add sequences for the button presses.

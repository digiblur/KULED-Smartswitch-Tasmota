# KULED-Smartswitch-Tasmota
The KULED WiFi Smartswitch unboxing and Tasmota firmware flashing tutorial.

Video of the Sonoff Hydra-Basic and Setup - https://www.youtube.com/watch?v=4nX90vhAniQ

### Parts List
- [KULED SmartSwitch (2 Pack)](https://amzn.to/2JqvWd6) 
- [or 4 pack](https://amzn.to/2Odbc9v)
- [USB FTDI Adapter to Flash the Unit](https://amzn.to/2Rpu9rx)
- [Male Headers](https://amzn.to/2JtX1fB)
- [Jumper Wires](https://amzn.to/2DcCiMX)

### Wiring Diagram
![alt text](https://raw.githubusercontent.com/digiblur/KULED-Smartswitch-Tasmota/master/GPIO%20PINS.jpg "Wiring Diagram")

### HomeAssistant Binary Sensor Config YAML
```yaml
- platform: mqtt
  name: "KuLED Test"
  state_topic: "stat/KULED-1/POWER"
  command_topic: "cmnd/KULED-1/POWER"
  availability_topic: "tele/KULED-1/LWT"
  qos: 1
  payload_on: "ON"
  payload_off: "OFF"
  payload_available: "Online"
  payload_not_available: "Offline"
  retain: false
```

### Disclaimer
:warning: **DANGER OF ELECTROCUTION** :warning:

The dimmer uses Mains AC power!  There is a danger of electrocution if not installed properly. If you don't know how to install it, please call an electrician. Remember: _**SAFETY FIRST**_. It is not worth to risk yourself, your family and your home if you don't know exactly what you are doing. Never try to flash, open, or service the dimmer device while it is connected to any power source.

We don't take any responsibility nor liability for using this software nor for the installation or any tips, advice, videos, etc. given by anyone on this site or any other site.

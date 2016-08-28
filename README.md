# githass
## Home Assistant Configuration
Currently running on 3rd gen RaspberryPi (OS: Raspbian Jessie)

###Components Used:
- Forecast.io and Wunderground for weather
- NMAP Device Tracking
- Ecobee3 Thermostat + 1 Remote Sensor
- Wink Hub
  - 3 Cree Connected Bulbs (Zigbee)
  -  7 GE Link Bulbs (Zigbee)
- NVIDIA Shield TV
- PLEX Server

###Automations:
- Light control based on device presence and sun status
- Theromstat control based on outside temperature and device presence (away mode)

###Notes:
1. I use secrets.yaml to hide sensitive information (like API keys)
2. Currently, Home Assistant has ZERO local control over devices (Wink talks to cloud, Ecobee talks to cloud).  My goal is to force everything to be local so if the interenet goes out, my home will still be automated.
  * This implies either a custom zigbee implementation to control lights or a local-only zigbee hub like Phillips Hue.  The downside being that I'd ALSO need to get a zwave radio to interface with future zwave components.  Another option would be to root the wink hub to force local-only control.
 
###Future Improvements:
- ~~Automation override switches~~ (added 8/21/2016)
- ~~Rapberry pi status monitoring~~ (added 8/27/2016)
- Integrate Alexa (![emulated_hue}(https://home-assistant.io/components/emulated_hue/) looks promising)
- Selectable scenes
- Vacation Modes
- More components:
  - Home weather station (to replace forecast.io)
  - Lights/switches
  - Door/window sensors
  - IP Cameras
  - Sprinkler/Irrigation automation
  - [Washer/dryer status](https://home-assistant.io/blog/2016/08/03/laundry-automation-update/) (custom sensor, probably)
  - Dishwasher status (custom sensor, probably)
  
Current setup cost estimate: $500 

(Images last updated 8/27/2016, may not reflect current configuration)
![](https://github.com/fronzbot/githass/blob/master/images/ha_home_page.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_media.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_thermostat.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_presence.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_weather1.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_weather2.png)
![](https://github.com/fronzbot/githass/blob/master/images/ha_presences.png)

# HomeAssistant Config

This is my current HomeAssistant config running on a Raspberry Pi 3.

Regular Blog posts about my Home Automation setup here: http://www.handmadepixels.co.uk/blog/

**Devices:**

 - iOS Devices
 - Tado Smart Thermostat v3
 - Tado Smart Radiator Thermostat
 - Philips Hue Hub v2
 - Philips Hue Bulbs
 - NodeMCU (ESP8266) with DS18B20 Temp Sensor
 - Netgear R7000 Nighthack with ASUS-WRT Vortex Firmware
 - Raspberry Pi 1B Running PiHole
 - Samsung Smart TV
 - Logitech Harmony Elite Remote and Hub
 - Raspberry Pi 2B Running Kodi (OSMC)

**Additional Software Packages:**
These packages are installed on the Raspberry Pi hosting Home Assistant 

 - HomeBridge - exposing Home Assistant and Logitech Harmony Hub to iOS HomeKit
 - Mosquitto - MQTT broker connected into Home Assistant
 - Transmission
 - OpenVPN

**Automations:**

*Lights*
 - Switch on Front Door & Landing lights at sunset if no one home
 - Switch on Lounge & Dining Room lights 1 hour before sunset if someone is home
 - Switch on Lounge & Dining Room lights when someone arrives home if lights not already on and 1 hour before sunset
 - Switch on Front Door light when Cat arrives home between 10pm and 6am
 - Switch off all lights 5 minutes after everyone leaves the house but only if after 7am, 15 minutes before sunset and if Guest Mode is not enabled
 - Switch off Front Door light 10 minutes after arriving home
 - Switch on Office Light Strip when Windows PC is switched on
 - Switch off Office Light Strip when Windows PC is switched off
 - Switch on Office Light Strip when Working From Home Mode is enabled
 
*Notifications*
 - Send iOS notification warning me if the disk space usage on Raspberry Pi is greater than 90%
 - Send iOS notification informing me of my commute to work time at 7am, repeat 2 times with 30 min delay
 - Send iOS notification at 4:30pm with Commute Home time, repeat 2 times with 30 min delay (Information)
 - Send iOS notification when Home Assistant Starts (Information)
 - Send iOS notification when Update for Home Assistant is available, this also creates a persistant tile on the Web Front End
 - Send iOS notification 15 minutes before sunset or when I arrive home on a weekday and if current outside temp is less than 3 degrees informing me to put the windscreen cover on the car
 - Send Rich iOS notification at 8am if i am at on a weekday asking if i am working from home, if i respond "yes" the input boolean work_from_home is enabled
 - Send iOS notification is PiHole Raspberry Pi is offline
 
*Automation States*
 - Enable lights_on_after_hours automation if Cat is out of the house after 9pm
 - Disable lights_on_after_hours automation 10 minutes after Cat arrives home after 10pm and before 6am
 
*Input Boolean*
 - Enable input_boolean.gamingpc_online when WOL Switch state changes from OFF to ON (input boolean is used in office lights automation)
 - Disable input_boolean.gamingpc_online when WOL Switch state changes from ON to OFF (input boolean is used in office lights automation)
 
----------

**Home Assistant Web Front End:**

Still WIP and always changing, my web front end is all custom views, i try to group as many things as possible and then put the group into individual rooms groups to allow a quick overview of the home.

*Home Page*
![Home Page](http://i.imgur.com/WYNE52X.png)

*Lights Page*
![Lights Page](http://imgur.com/tLrW1qn.png)

*Settings Page*
![Settings Page](http://imgur.com/ynUQK7F.png)

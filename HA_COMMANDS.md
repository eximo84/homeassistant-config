# HomeAssistant Terminal Commands

**HomeAssistant Service Control:**

 - To check realtime logs: `sudo journalctl -fu home-assistant@hass.service`
 - To restart HomeAssistant: `sudo systemctl restart home-assistant@hass.service`
 - To check logs: `sudo systemctl status -l home-assistant@hass.service`
 - To stop HomeAssistant: `sudo systemctl stop home-assistant@hass.service`
 - To start HomeAssistant: `sudo systemctl start home-assistant@hass.service`

**Update HomeAssistant:**

 1. Change to homeassistant user: `sudo su -s /bin/bash homeassistant`
 2. Change to virtual enviroment: `source /srv/homeassistant/homeassistant_venv/bin/activate`
 3. Update HomeAssistant `pip3 install --upgrade homeassistant`
 4. Type `exit` to logout the homeassistant user and return to the pi user.
 5. Restart the HomeAssistant Service

**Push Changes to Git Repo**

 1. Navigate to homeassistant directory: `cd /home/homeassistant/.homeassistant`
 2. Change to homeassistant user: `sudo su -s /bin/bash homeassistant`
 3. `git add .`
 4. `git commit -m 'Commit Message'`
 5. `git push origin master`

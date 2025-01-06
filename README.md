# Obico2HomeAssistant
Send [Obico-Server](https://www.obico.io/docs/server-guides/) notifications to Home Assistant using Webhook automation

## My Setup:
* Ender 3 Pro
* [OctoPrint](https://octoprint.org/) running on Raspberry Pi 3B+ with Obico add-in
* Obico-Server running on Mini PC with Intel N100 Processor
* Home Assistant 

## Example App Notification:
<a href="url"><img src="https://github.com/user-attachments/assets/9d59ec4e-826d-4a46-b1eb-d219778c66f4" width="500" ></a>

## Configuration:
* Homeassistant: Settings => Automations => Blueprints
* Click "IMPORT BLUEPRINT" in the bottom right corner.
* Paste the following address: https://github.com/berkeoznalbant/Obico2HomeAssistant/blob/main/obico_blueprint.yaml
* Click preview and then click "Import Blueprint".
* Then choose the "Obico Webhook" from the blueprint list.
* Create a webhook ID for the automation that should be unique and hard to guess.
* In Obico go to Preference => Notifications => Webhook
* Paste the following link to Webhook URL section: http://<HOMEASSISTANT_IP>:<HOMEASSISTANT_PORT>/api/webhook/<WEBHOOK_ID>
* Get back to Home Assistant and choose the camera entity for the 3D printer.

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
* Homeassistant: Settings => Automations => New Automation
* Enable YAML Mode in the top right corner
* Paste Code from `obico.yaml` into automation
* Change the `webhook_id` to [something unique](https://www.uuidgenerator.net/)
* In the `PrintFailure` function, change the `device_id` to your printer camera
* You may want to change the path of the camera snapshot
* I personally use Home Assistant companion app for my notifications, you may wish to change the notifications to your liking
* Configure Obico-Server to use `Webhook` and point it at your Home Assistant `https://[HOMEASSISTANT URL HERE]/api/webhook/[WEBHOOK ID FROM AUTOMATION HERE]`

## Issues:
* Occasionally receive double notifications for prints starting?

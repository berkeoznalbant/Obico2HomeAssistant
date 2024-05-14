# Obico2HomeAssistant
Send [Obico-Server](https://www.obico.io/docs/server-guides/) notifications to Home Assistant using Webhook automation

## My Setup:
* Bambu Labs P1S v01.05.02.00 (in LAN mode)
* [OctoPrint](https://octoprint.org/) v1.10.0 with the [OctoPrint-BambuPrinter](https://github.com/jneilliii/OctoPrint-BambuPrinter/) v0.0.18 addin
* [go2rtc](https://github.com/AlexxIT/go2rtc) with the [bambu-go2rtc](https://github.com/synman/bambu-go2rtc) mod for the P1S camera
* Obico-Server running on Jetson Nano
* Home Assistant v2024.5.3

## Example Telegram Notification:
![Telegam Notification](https://raw.githubusercontent.com/johnc2k/Obico2HomeAssistant/main/Telegram%20Notification.PNG)

## Configuration:
* Homeassistant: Settings => Automations => New Automation
* Enable Yaml Mode in the top right corner
* Paste Code from `obico.yaml` into automation
* Change the `webhook_id` to [something unique](https://www.uuidgenerator.net/)
* In the `PrintFailure` function, change the `device_id` to your printer camera
* You may want to change the path of the camera snapshot
* I personally use Telegram for my notifications, you may wish to change the notifications to your liking
* Configure Obico-Server to use `Webhook` and point it at your Home Assistant `https://[HOMEASSISTANT URL HERE]/api/webhook/[WEBHOOK ID FROM AUTOMATION HERE]`

## Issues:
* Occasionally receive double notifications for prints starting?

# Obico2HomeAssistant
Send [Obico-Server](https://www.obico.io/docs/server-guides/) notifications to Home Assistant using Web Hook automation

## My Setup:
* Bambu Labs P1S v01.05.02.00 (in LAN mode)
* [OctoPrint](https://octoprint.org/) v1.10.0 with the [OctoPrint-BambuPrinter](https://github.com/jneilliii/OctoPrint-BambuPrinter/) v0.0.18 addin
* [go2rtc](https://github.com/AlexxIT/go2rtc) with the [bambu-go2rtc](https://github.com/synman/bambu-go2rtc) mod for the P1S camera
* Obico-Server running on Jetson Nano
* Home Assistant v2024.5.3

## Configuration:
* Change the `webhook_id` to [something unique](https://www.uuidgenerator.net/)
* In the `PrintFailure` function, change the `device_id` to your printer camera
* I personally use Telegram for my notifications, you may wish to change the notifications to your liking

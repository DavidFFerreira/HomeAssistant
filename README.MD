# 🏠 David Ferreira - Home Assistant Configuration

<img align="right" src="https://www.home-assistant.io/images/favicon-192x192-full.png">

This is my [Home Assistant](https://www.home-assistant.io/) configuration - based on many of the other great configurations are out there (and listed below)

I live in ![Portugal](http://flags.ox3.in/mini/pt.png) so some of what you find here may not be relevent, or you may have access to better (and probably cheaper) ways.

It's very much a work-in-progress, but feel free to steal ideas or code to use for your own setup

_Please :star: this repo if you find it useful_

[![HA Version](https://img.shields.io/badge/Home%20Assistant--brightgreen)](https://github.com/home-assistant/home-assistant/releases/)
![GitHub last commit](https://img.shields.io/github/last-commit/bacco007/HomeAssistantConfig?style=flat-square) ![GitHub commit activity](https://img.shields.io/github/commit-activity/w/bacco007/HomeAssistantConfig?style=flat-square)
![Licence](https://img.shields.io/badge/license-Unlicense-blue.svg?style=flat-square)

![image](https://user-images.githubusercontent.com/32928749/189365835-60fbf4ef-b4fd-40a2-87df-c42eca44ccd6.png)

---

- [🏠TBSmartHome - Home Assistant Configuration](#tbsmarthome---home-assistant-configuration)
  - [Table of Contents](#table-of-contents)
  - [TL;DR](#tldr)
  - [Ecosystem](#ecosystem)
    - [Hardware](#hardware)
    - [Zigbee](#zigbee)
  - [Stats](#stats)
  - [Integrations Used](#integrations-used)
    - [Custom Components Used](#custom-components-used)
  - [Screenshots](#screenshots)
  - [HA Supervisor](#ha-supervisor)
    - [Addon Repositories](#addon-repositories)
    - [Addons](#addons)
  - [Licence](#licence)
  - [Other Good HA Resources/Configs](#other-good-ha-resourcesconfigs)
  
  
  ---


## TL;DR

This is my Home Assistant config - documentation isn't my strongest skill, so if you've got any questions, hit me up

<p align="right"><a href="#top" title="Back to top">Top</a></p>

## Ecosystem

My smarthome setup seems to be ever-growing, but at this stage it's unlikely that I'll make any major changes from here

### Hardware

- Dell Optiplex 7060 SFF (i5 8500T, 16Gb RAM, 254Gb HDD) running Proxmox
  - VM with Debian 11 for Home Assistant Supervisor + Hacs + Docker + Portainer
  - LXC Container with PLEX + Sonarr + Radarr + qBitTorrent + other usefull stuff
  - LXC Container with Adgard
  - LXC Container with OpenVPN
  - VM with Debian 11 for test stuff

### Zigbee

I'm running a combination of Chinese sensors for doors, Aqara for movement, switchs and modules from several chinese brands and a ZZH (CC2652R) as the host in Zigbee2Mqtt
I also use alot of Phlips hue Bulds coneected to a few Hue Bridges
To control some lights, I have 2 remote zigbee controlers, that can control light temperature and color, also have more 2 Hue dim remote controlers and 1 6 button remote controler and another 4 buttons remote handy switch
<p align="right"><a href="#top" title="Back to top">Top</a></p>

### WIFI

I'm running a combination of Chinese Routers like Xiaomi AX3200 and Redmi AX6 for mesh and good WIFI6 and a powerfull UDR-EU :P
This allow me to connect my Phones and a few chinese devices to my WIFI without struggle

![image](https://user-images.githubusercontent.com/32928749/189404303-2cab5e94-b3e6-49d1-8041-d50b30fcee1d.png)

---

## Stats

_Stats as at 21:00, Friday, October 09rd 2022_

| HA Version                               | No. Integrations                                        | No. Entities | No. Sensors | No. Automations |
| ---------------------------------------- | ------------------------------------------------------- | ------------ | ----------- | --------------- |
| 2022.9.1 | 110     | 663         | 361 | 19 |

Type | Qty
-- | --
Alarm Control Panel | 1
Alert | 0
Automation | 19
Binary Sensor | 75
Camera | 1
Device Tracker | 8
Group | 14
Input Boolean | 8
Input Datetime | 1
Input Text | 0
input Select | 3
Light | 80
Media Player | 12
Person | 3
Scene | 2
Script | 5
Sensor | 361
Sun | 1
Switch | 64
Weather | 2
Zone | 14

<p align="right"><a href="#top" title="Back to top">Top</a></p>

---


## Integrations Used

Here is a list of all the integrations I use, including any Custom Components (which are also listed below)
<details>
<summary>Expand Integrations List</summary>

| Name |
| --- |
| [adaptive_lighting](https://www.home-assistant.io/components/adaptive_lighting) |
| [adguard](https://www.home-assistant.io/components/adguard) |
| [alarm_control_panel](https://www.home-assistant.io/components/alarm_control_panel) |
| [analytics](https://www.home-assistant.io/components/analytics) |
| [androidtv](https://www.home-assistant.io/components/androidtv) |
| [api](https://www.home-assistant.io/components/api) |
| [application_credentials](https://www.home-assistant.io/components/application_credentials) |
| [psa_controller](https://github.com/flobz/psacc-ha/tree/main/psacc-ha) |
| [auth](https://www.home-assistant.io/components/auth) |
| [automation](https://www.home-assistant.io/components/automation) |
| [binary_sensor](https://www.home-assistant.io/components/binary_sensor) |
| [binary_sensor.cloud](https://www.home-assistant.io/components/binary_sensor.cloud) |
| [binary_sensor.esphome](https://www.home-assistant.io/components/binary_sensor.esphome) |
| [binary_sensor.hassio](https://www.home-assistant.io/components/binary_sensor.hassio) |
| [binary_sensor.iss](https://www.home-assistant.io/components/binary_sensor.iss) |
| [binary_sensor.mobile_app](https://www.home-assistant.io/components/binary_sensor.mobile_app) |
| [binary_sensor.mqtt](https://www.home-assistant.io/components/binary_sensor.mqtt) |
| [binary_sensor.openuv](https://www.home-assistant.io/components/binary_sensor.openuv) |
| [binary_sensor.ping](https://www.home-assistant.io/components/binary_sensor.ping) |
| [binary_sensor.proxmoxve](https://www.home-assistant.io/components/binary_sensor.proxmoxve) |
| [binary_sensor.sensibo](https://www.home-assistant.io/components/binary_sensor.sensibo) |
| [binary_sensor.sun2](https://www.home-assistant.io/components/binary_sensor.sun2) |
| [binary_sensor.template](https://www.home-assistant.io/components/binary_sensor.template) |
| [binary_sensor.tod](https://www.home-assistant.io/components/binary_sensor.tod) |
| [binary_sensor.tuya](https://www.home-assistant.io/components/binary_sensor.tuya) |
| [binary_sensor.upnp](https://www.home-assistant.io/components/binary_sensor.upnp) |
| [binary_sensor.upnp_availability](https://www.home-assistant.io/components/binary_sensor.upnp_availability) |
| [binary_sensor.uptime_kuma](https://www.home-assistant.io/components/binary_sensor.uptime_kuma) |
| [binary_sensor.version](https://www.home-assistant.io/components/binary_sensor.version) |
| [binary_sensor.weatherflow](https://www.home-assistant.io/components/binary_sensor.weatherflow) |
| [binary_sensor.workday](https://www.home-assistant.io/components/binary_sensor.workday) |
| [blueprint](https://www.home-assistant.io/components/blueprint) |
| [bureau_of_meteorology](https://www.home-assistant.io/components/bureau_of_meteorology) |
| [button](https://www.home-assistant.io/components/button) |
| [button.esphome](https://www.home-assistant.io/components/button.esphome) |
| [button.mqtt](https://www.home-assistant.io/components/button.mqtt) |
| [button.plex](https://www.home-assistant.io/components/button.plex) |
| [button.tuya](https://www.home-assistant.io/components/button.tuya) |
| [calendar](https://www.home-assistant.io/components/calendar) |
| [calendar.garbage_collection](https://www.home-assistant.io/components/calendar.garbage_collection) |
| [calendar.holidays](https://www.home-assistant.io/components/calendar.holidays) |
| [calendar.ical](https://www.home-assistant.io/components/calendar.ical) |
| [camera](https://www.home-assistant.io/components/camera) |
| [camera.mqtt](https://www.home-assistant.io/components/camera.mqtt) |
| [camera.tuya](https://www.home-assistant.io/components/camera.tuya) |
| [cast](https://www.home-assistant.io/components/cast) |
| [cert_expiry](https://www.home-assistant.io/components/cert_expiry) |
| [climate](https://www.home-assistant.io/components/climate) |
| [climate.mqtt](https://www.home-assistant.io/components/climate.mqtt) |
| [climate.sensibo](https://www.home-assistant.io/components/climate.sensibo) |
| [climate.tuya](https://www.home-assistant.io/components/climate.tuya) |
| [cloud](https://www.home-assistant.io/components/cloud) |
| [co2signal](https://www.home-assistant.io/components/co2signal) |
| [config](https://www.home-assistant.io/components/config) |
| [counter](https://www.home-assistant.io/components/counter) |
| [cover](https://www.home-assistant.io/components/cover) |
| [cover.mqtt](https://www.home-assistant.io/components/cover.mqtt) |
| [cover.tuya](https://www.home-assistant.io/components/cover.tuya) |
| [cover.zha](https://www.home-assistant.io/components/cover.zha) |
| [cupertino](https://www.home-assistant.io/components/cupertino) |
| [default_config](https://www.home-assistant.io/components/default_config) |
| [device_automation](https://www.home-assistant.io/components/device_automation) |
| [device_tracker.mqtt](https://www.home-assistant.io/components/device_tracker.mqtt) |
| [dhcp](https://www.home-assistant.io/components/dhcp) |
| [diagnostics](https://www.home-assistant.io/components/diagnostics) |
| [dwains_dashboard](https://www.home-assistant.io/components/dwains_dashboard) |
| [dyson_local](https://www.home-assistant.io/components/dyson_local) |
| [energy](https://www.home-assistant.io/components/energy) |
| [esphome](https://www.home-assistant.io/components/esphome) |
| [favicon](https://www.home-assistant.io/components/favicon) |
| [ffmpeg](https://www.home-assistant.io/components/ffmpeg) |
| [fontawesome](https://www.home-assistant.io/components/fontawesome) |
| [forecast_solar](https://www.home-assistant.io/components/forecast_solar) |
| [frontend](https://www.home-assistant.io/components/frontend) |
| [garbage_collection](https://www.home-assistant.io/components/garbage_collection) |
| [gdacs](https://www.home-assistant.io/components/gdacs) |
| [geo_location](https://www.home-assistant.io/components/geo_location) |
| [geo_location.blitzortung](https://www.home-assistant.io/components/geo_location.blitzortung) |
| [geo_location.gdacs](https://www.home-assistant.io/components/geo_location.gdacs) |
| [geo_location.nsw_rural_fire_service_feed](https://www.home-assistant.io/components/geo_location.nsw_rural_fire_service_feed) |
| [github](https://www.home-assistant.io/components/github) |
| [glances](https://www.home-assistant.io/components/glances) |
| [group](https://www.home-assistant.io/components/group) |
| [hacs](https://www.home-assistant.io/components/hacs) |
| [harmony](https://www.home-assistant.io/components/harmony) |
| [hassio](https://www.home-assistant.io/components/hassio) |
| [http](https://www.home-assistant.io/components/http) |
| [iaquk](https://www.home-assistant.io/components/iaquk) |
| [ical](https://www.home-assistant.io/components/ical) |
| [ifttt](https://www.home-assistant.io/components/ifttt) |
| [image](https://www.home-assistant.io/components/image) |
| [influxdb](https://www.home-assistant.io/components/influxdb) |
| [input_boolean](https://www.home-assistant.io/components/input_boolean) |
| [input_button](https://www.home-assistant.io/components/input_button) |
| [input_datetime](https://www.home-assistant.io/components/input_datetime) |
| [input_number](https://www.home-assistant.io/components/input_number) |
| [input_select](https://www.home-assistant.io/components/input_select) |
| [input_text](https://www.home-assistant.io/components/input_text) |
| [launch_library](https://www.home-assistant.io/components/launch_library) |
| [light](https://www.home-assistant.io/components/light) |
| [light.group](https://www.home-assistant.io/components/light.group) |
| [light.mqtt](https://www.home-assistant.io/components/light.mqtt) |
| [light.tuya](https://www.home-assistant.io/components/light.tuya) |
| [lock](https://www.home-assistant.io/components/lock) |
| [lock.mqtt](https://www.home-assistant.io/components/lock.mqtt) |
| [logbook](https://www.home-assistant.io/components/logbook) |
| [logger](https://www.home-assistant.io/components/logger) |
| [lovelace](https://www.home-assistant.io/components/lovelace) |
| [map](https://www.home-assistant.io/components/map) |
| [media_player](https://www.home-assistant.io/components/media_player) |
| [media_player.androidtv](https://www.home-assistant.io/components/media_player.androidtv) |
| [media_player.cast](https://www.home-assistant.io/components/media_player.cast) |
| [media_player.dlna_dmr](https://www.home-assistant.io/components/media_player.dlna_dmr) |
| [media_player.plex](https://www.home-assistant.io/components/media_player.plex) |
| [media_player.spotify](https://www.home-assistant.io/components/media_player.spotify) |
| [media_source](https://www.home-assistant.io/components/media_source) |
| [mobile_app](https://www.home-assistant.io/components/mobile_app) |
| [monitor_docker](https://www.home-assistant.io/components/monitor_docker) |
| [moon](https://www.home-assistant.io/components/moon) |
| [mqtt](https://www.home-assistant.io/components/mqtt) |
| [my](https://www.home-assistant.io/components/my) |
| [myjdownloader](https://www.home-assistant.io/components/myjdownloader) |
| [network](https://www.home-assistant.io/components/network) |
| [nfl](https://www.home-assistant.io/components/nfl) |
| [nhl](https://www.home-assistant.io/components/nhl) |
| [nodered](https://www.home-assistant.io/components/nodered) |
| [notify](https://www.home-assistant.io/components/notify) |
| [notify.group](https://www.home-assistant.io/components/notify.group) |
| [notify.ios](https://www.home-assistant.io/components/notify.ios) |
| [notify.mobile_app](https://www.home-assistant.io/components/notify.mobile_app) |
| [notify.slack](https://www.home-assistant.io/components/notify.slack) |
| [number](https://www.home-assistant.io/components/number) |
| [number.mqtt](https://www.home-assistant.io/components/number.mqtt) |
| [number.sensibo](https://www.home-assistant.io/components/number.sensibo) |
| [number.sonos](https://www.home-assistant.io/components/number.sonos) |
| [number.tuya](https://www.home-assistant.io/components/number.tuya) |
| [number.zha](https://www.home-assistant.io/components/number.zha) |
| [onboarding](https://www.home-assistant.io/components/onboarding) |
| [opennem](https://www.home-assistant.io/components/opennem) |
| [openuv](https://www.home-assistant.io/components/openuv) |
| [panel_iframe](https://www.home-assistant.io/components/panel_iframe) |
| [persistent_notification](https://www.home-assistant.io/components/persistent_notification) |
| [person](https://www.home-assistant.io/components/person) |
| [ping](https://www.home-assistant.io/components/ping) |
| [plex](https://www.home-assistant.io/components/plex) |
| [proxmoxve](https://www.home-assistant.io/components/proxmoxve) |
| [pyscript](https://www.home-assistant.io/components/pyscript) |
| [python_script](https://www.home-assistant.io/components/python_script) |
| [radarr](https://www.home-assistant.io/components/radarr) |
| [radio_browser](https://www.home-assistant.io/components/radio_browser) |
| [readme](https://www.home-assistant.io/components/readme) |
| [recorder](https://www.home-assistant.io/components/recorder) |
| [remote](https://www.home-assistant.io/components/remote) |
| [remote.apple_tv](https://www.home-assistant.io/components/remote.apple_tv) |
| [remote.broadlink](https://www.home-assistant.io/components/remote.broadlink) |
| [remote.harmony](https://www.home-assistant.io/components/remote.harmony) |
| [remote.xbox](https://www.home-assistant.io/components/remote.xbox) |
| [rest](https://www.home-assistant.io/components/rest) |
| [rocketlaunchlive](https://www.home-assistant.io/components/rocketlaunchlive) |
| [sabnzbd](https://www.home-assistant.io/components/sabnzbd) |
| [samsungtv](https://www.home-assistant.io/components/samsungtv) |
| [samsungtv_smart](https://www.home-assistant.io/components/samsungtv_smart) |
| [satellitetracker](https://www.home-assistant.io/components/satellitetracker) |
| [scene](https://www.home-assistant.io/components/scene) |
| [scene.homeassistant](https://www.home-assistant.io/components/scene.homeassistant) |
| [scene.mqtt](https://www.home-assistant.io/components/scene.mqtt) |
| [scene.tuya](https://www.home-assistant.io/components/scene.tuya) |
| [script](https://www.home-assistant.io/components/script) |
| [search](https://www.home-assistant.io/components/search) |
| [season](https://www.home-assistant.io/components/season) |
| [select](https://www.home-assistant.io/components/select) |
| [select.dyson_local](https://www.home-assistant.io/components/select.dyson_local) |
| [select.eufy_security](https://www.home-assistant.io/components/select.eufy_security) |
| [select.harmony](https://www.home-assistant.io/components/select.harmony) |
| [select.mqtt](https://www.home-assistant.io/components/select.mqtt) |
| [select.sensibo](https://www.home-assistant.io/components/select.sensibo) |
| [select.tuya](https://www.home-assistant.io/components/select.tuya) |
| [select.zha](https://www.home-assistant.io/components/select.zha) |
| [sensibo](https://www.home-assistant.io/components/sensibo) |
| [sensor](https://www.home-assistant.io/components/sensor) |
| [sensor.adguard](https://www.home-assistant.io/components/sensor.adguard) |
| [sensor.anniversaries](https://www.home-assistant.io/components/sensor.anniversaries) |
| [sensor.aus_fuel](https://www.home-assistant.io/components/sensor.aus_fuel) |
| [sensor.authenticated](https://www.home-assistant.io/components/sensor.authenticated) |
| [sensor.average](https://www.home-assistant.io/components/sensor.average) |
| [sensor.blitzortung](https://www.home-assistant.io/components/sensor.blitzortung) |
| [sensor.broadlink](https://www.home-assistant.io/components/sensor.broadlink) |
| [sensor.bureau_of_meteorology](https://www.home-assistant.io/components/sensor.bureau_of_meteorology) |
| [sensor.cert_expiry](https://www.home-assistant.io/components/sensor.cert_expiry) |
| [sensor.co2signal](https://www.home-assistant.io/components/sensor.co2signal) |
| [sensor.command_line](https://www.home-assistant.io/components/sensor.command_line) |
| [sensor.doomsday_clock](https://www.home-assistant.io/components/sensor.doomsday_clock) |
| [sensor.dwains_dashboard](https://www.home-assistant.io/components/sensor.dwains_dashboard) |
| [sensor.dyson_local](https://www.home-assistant.io/components/sensor.dyson_local) |
| [sensor.energy](https://www.home-assistant.io/components/sensor.energy) |
| [sensor.esphome](https://www.home-assistant.io/components/sensor.esphome) |
| [sensor.eufy_security](https://www.home-assistant.io/components/sensor.eufy_security) |
| [sensor.feedparser](https://www.home-assistant.io/components/sensor.feedparser) |
| [sensor.forecast_solar](https://www.home-assistant.io/components/sensor.forecast_solar) |
| [sensor.formulaone_api](https://www.home-assistant.io/components/sensor.formulaone_api) |
| [sensor.garbage_collection](https://www.home-assistant.io/components/sensor.garbage_collection) |
| [sensor.gdacs](https://www.home-assistant.io/components/sensor.gdacs) |
| [sensor.github](https://www.home-assistant.io/components/sensor.github) |
| [sensor.glances](https://www.home-assistant.io/components/sensor.glances) |
| [sensor.google_fit](https://www.home-assistant.io/components/sensor.google_fit) |
| [sensor.hacs](https://www.home-assistant.io/components/sensor.hacs) |
| [sensor.hassio](https://www.home-assistant.io/components/sensor.hassio) |
| [sensor.hdhomerun](https://www.home-assistant.io/components/sensor.hdhomerun) |
| [sensor.here_travel_time](https://www.home-assistant.io/components/sensor.here_travel_time) |
| [sensor.iaquk](https://www.home-assistant.io/components/sensor.iaquk) |
| [sensor.ical](https://www.home-assistant.io/components/sensor.ical) |
| [sensor.integration](https://www.home-assistant.io/components/sensor.integration) |
| [sensor.ios](https://www.home-assistant.io/components/sensor.ios) |
| [sensor.jellyfin](https://www.home-assistant.io/components/sensor.jellyfin) |
| [sensor.launch_library](https://www.home-assistant.io/components/sensor.launch_library) |
| [sensor.mobile_app](https://www.home-assistant.io/components/sensor.mobile_app) |
| [sensor.monitor_docker](https://www.home-assistant.io/components/sensor.monitor_docker) |
| [sensor.moon](https://www.home-assistant.io/components/sensor.moon) |
| [sensor.mqtt](https://www.home-assistant.io/components/sensor.mqtt) |
| [sensor.myjdownloader](https://www.home-assistant.io/components/sensor.myjdownloader) |
| [sensor.nfl](https://www.home-assistant.io/components/sensor.nfl) |
| [sensor.nhl](https://www.home-assistant.io/components/sensor.nhl) |
| [sensor.nodered](https://www.home-assistant.io/components/sensor.nodered) |
| [sensor.nsw_air_quality](https://www.home-assistant.io/components/sensor.nsw_air_quality) |
| [sensor.nsw_fuel_station](https://www.home-assistant.io/components/sensor.nsw_fuel_station) |
| [sensor.nsw_rural_fire_service_fire_danger](https://www.home-assistant.io/components/sensor.nsw_rural_fire_service_fire_danger) |
| [sensor.opennem](https://www.home-assistant.io/components/sensor.opennem) |
| [sensor.openuv](https://www.home-assistant.io/components/sensor.openuv) |
| [sensor.plex](https://www.home-assistant.io/components/sensor.plex) |
| [sensor.plex_recently_added](https://www.home-assistant.io/components/sensor.plex_recently_added) |
| [sensor.radarr](https://www.home-assistant.io/components/sensor.radarr) |
| [sensor.radarr_upcoming_media](https://www.home-assistant.io/components/sensor.radarr_upcoming_media) |
| [sensor.rest](https://www.home-assistant.io/components/sensor.rest) |
| [sensor.rocketlaunchlive](https://www.home-assistant.io/components/sensor.rocketlaunchlive) |
| [sensor.sabnzbd](https://www.home-assistant.io/components/sensor.sabnzbd) |
| [sensor.satellitetracker](https://www.home-assistant.io/components/sensor.satellitetracker) |
| [sensor.scrape](https://www.home-assistant.io/components/sensor.scrape) |
| [sensor.season](https://www.home-assistant.io/components/sensor.season) |
| [sensor.sensibo](https://www.home-assistant.io/components/sensor.sensibo) |
| [sensor.smartthinq_sensors](https://www.home-assistant.io/components/sensor.smartthinq_sensors) |
| [sensor.snmp](https://www.home-assistant.io/components/sensor.snmp) |
| [sensor.solcast_solar](https://www.home-assistant.io/components/sensor.solcast_solar) |
| [sensor.sonarr](https://www.home-assistant.io/components/sensor.sonarr) |
| [sensor.sonarr_upcoming_media](https://www.home-assistant.io/components/sensor.sonarr_upcoming_media) |
| [sensor.sonos](https://www.home-assistant.io/components/sensor.sonos) |
| [sensor.spacex](https://www.home-assistant.io/components/sensor.spacex) |
| [sensor.speedtestdotnet](https://www.home-assistant.io/components/sensor.speedtestdotnet) |
| [sensor.sql](https://www.home-assistant.io/components/sensor.sql) |
| [sensor.statistics](https://www.home-assistant.io/components/sensor.statistics) |
| [sensor.sun2](https://www.home-assistant.io/components/sensor.sun2) |
| [sensor.systemmonitor](https://www.home-assistant.io/components/sensor.systemmonitor) |
| [sensor.tautulli](https://www.home-assistant.io/components/sensor.tautulli) |
| [sensor.template](https://www.home-assistant.io/components/sensor.template) |
| [sensor.thermal_comfort](https://www.home-assistant.io/components/sensor.thermal_comfort) |
| [sensor.time_date](https://www.home-assistant.io/components/sensor.time_date) |
| [sensor.tomorrowio](https://www.home-assistant.io/components/sensor.tomorrowio) |
| [sensor.trakt_tv](https://www.home-assistant.io/components/sensor.trakt_tv) |
| [sensor.transmission](https://www.home-assistant.io/components/sensor.transmission) |
| [sensor.transport_nsw](https://www.home-assistant.io/components/sensor.transport_nsw) |
| [sensor.tuya](https://www.home-assistant.io/components/sensor.tuya) |
| [sensor.unifigateway](https://www.home-assistant.io/components/sensor.unifigateway) |
| [sensor.untappd](https://www.home-assistant.io/components/sensor.untappd) |
| [sensor.upnp](https://www.home-assistant.io/components/sensor.upnp) |
| [sensor.uptime](https://www.home-assistant.io/components/sensor.uptime) |
| [sensor.version](https://www.home-assistant.io/components/sensor.version) |
| [sensor.waqi](https://www.home-assistant.io/components/sensor.waqi) |
| [sensor.watchman](https://www.home-assistant.io/components/sensor.watchman) |
| [sensor.waternsw](https://www.home-assistant.io/components/sensor.waternsw) |
| [sensor.waze_travel_time](https://www.home-assistant.io/components/sensor.waze_travel_time) |
| [sensor.weatherflow](https://www.home-assistant.io/components/sensor.weatherflow) |
| [sensor.worldclock](https://www.home-assistant.io/components/sensor.worldclock) |
| [shell_command](https://www.home-assistant.io/components/shell_command) |
| [simpleicons](https://www.home-assistant.io/components/simpleicons) |
| [siren](https://www.home-assistant.io/components/siren) |
| [siren.mqtt](https://www.home-assistant.io/components/siren.mqtt) |
| [siren.tuya](https://www.home-assistant.io/components/siren.tuya) |
| [slack](https://www.home-assistant.io/components/slack) |
| [smartthinq_sensors](https://www.home-assistant.io/components/smartthinq_sensors) |
| [solcast_solar](https://www.home-assistant.io/components/solcast_solar) |
| [sonarr](https://www.home-assistant.io/components/sonarr) |
| [sonos](https://www.home-assistant.io/components/sonos) |
| [spacex](https://www.home-assistant.io/components/spacex) |
| [speedtestdotnet](https://www.home-assistant.io/components/speedtestdotnet) |
| [spotify](https://www.home-assistant.io/components/spotify) |
| [sql](https://www.home-assistant.io/components/sql) |
| [ssdp](https://www.home-assistant.io/components/ssdp) |
| [stream](https://www.home-assistant.io/components/stream) |
| [stt](https://www.home-assistant.io/components/stt) |
| [sun](https://www.home-assistant.io/components/sun) |
| [switch](https://www.home-assistant.io/components/switch) |
| [switch.adaptive_lighting](https://www.home-assistant.io/components/switch.adaptive_lighting) |
| [switch.adguard](https://www.home-assistant.io/components/switch.adguard) |
| [switch.esphome](https://www.home-assistant.io/components/switch.esphome) |
| [switch.monitor_docker](https://www.home-assistant.io/components/switch.monitor_docker) |
| [switch.mqtt](https://www.home-assistant.io/components/switch.mqtt) |
| [switch.myjdownloader](https://www.home-assistant.io/components/switch.myjdownloader) |
| [switch.nodered](https://www.home-assistant.io/components/switch.nodered) |
| [switch.template](https://www.home-assistant.io/components/switch.template) |
| [switch.transmission](https://www.home-assistant.io/components/switch.transmission) |
| [switch.tuya](https://www.home-assistant.io/components/switch.tuya) |
| [system_health](https://www.home-assistant.io/components/system_health) |
| [system_log](https://www.home-assistant.io/components/system_log) |
| [tag](https://www.home-assistant.io/components/tag) |
| [tautulli](https://www.home-assistant.io/components/tautulli) |
| [template](https://www.home-assistant.io/components/template) |
| [thermal_comfort](https://www.home-assistant.io/components/thermal_comfort) |
| [timer](https://www.home-assistant.io/components/timer) |
| [tomorrowio](https://www.home-assistant.io/components/tomorrowio) |
| [trace](https://www.home-assistant.io/components/trace) |
| [trakt_tv](https://www.home-assistant.io/components/trakt_tv) |
| [transmission](https://www.home-assistant.io/components/transmission) |
| [tts](https://www.home-assistant.io/components/tts) |
| [tts.cloud](https://www.home-assistant.io/components/tts.cloud) |
| [tts.google_translate](https://www.home-assistant.io/components/tts.google_translate) |
| [tuya](https://www.home-assistant.io/components/tuya) |
| [unifi](https://www.home-assistant.io/components/unifi) |
| [update](https://www.home-assistant.io/components/update) |
| [update.hacs](https://www.home-assistant.io/components/update.hacs) |
| [update.hassio](https://www.home-assistant.io/components/update.hassio) |
| [update.hdhomerun](https://www.home-assistant.io/components/update.hdhomerun) |
| [update.myjdownloader](https://www.home-assistant.io/components/update.myjdownloader) |
| [update.sensibo](https://www.home-assistant.io/components/update.sensibo) |
| [update.synology_dsm](https://www.home-assistant.io/components/update.synology_dsm) |
| [update.unifi](https://www.home-assistant.io/components/update.unifi) |
| [upnp](https://www.home-assistant.io/components/upnp) |
| [upnp_availability](https://www.home-assistant.io/components/upnp_availability) |
| [uptime](https://www.home-assistant.io/components/uptime) |
| [uptime_kuma](https://www.home-assistant.io/components/uptime_kuma) |
| [usb](https://www.home-assistant.io/components/usb) |
| [vacuum](https://www.home-assistant.io/components/vacuum) |
| [vacuum.mqtt](https://www.home-assistant.io/components/vacuum.mqtt) |
| [vacuum.tuya](https://www.home-assistant.io/components/vacuum.tuya) |
| [version](https://www.home-assistant.io/components/version) |
| [watchman](https://www.home-assistant.io/components/watchman) |
| [waze_travel_time](https://www.home-assistant.io/components/waze_travel_time) |
| [weather](https://www.home-assistant.io/components/weather) |
| [weather.bureau_of_meteorology](https://www.home-assistant.io/components/weather.bureau_of_meteorology) |
| [weather.darksky](https://www.home-assistant.io/components/weather.darksky) |
| [weather.template](https://www.home-assistant.io/components/weather.template) |
| [weather.tomorrowio](https://www.home-assistant.io/components/weather.tomorrowio) |
| [weather.weatherflow](https://www.home-assistant.io/components/weather.weatherflow) |
| [weatherflow](https://www.home-assistant.io/components/weatherflow) |
| [webhook](https://www.home-assistant.io/components/webhook) |
| [websocket_api](https://www.home-assistant.io/components/websocket_api) |
| [zeroconf](https://www.home-assistant.io/components/zeroconf) |
| [zone](https://www.home-assistant.io/components/zone) |
</details>

<details>
<summary>Expand Devices list</summary>
  
| Name |
| --- |
| [Zigbee Hub CC2652R ZZH](https://electrolama.com/projects/zig-a-zig-ah/) |
| [OptiPlex 7060 Micro](https://www.dell.com/pt/empresas/p/optiplex-7060-micro/pd) |
| [Router Mesh Xiaomi AX3200](https://www.pcdiga.com/router-xiaomi-alot-ax3200-dual-band-wifi-6-gigabit-x-dvb4314gl) |
| [Router Mesh Redmi AX6](https://xiaomi-mi.com/wifi-routers/redmi-ax6-router/) |
| [Router Ubiquiti UDR-EU](https://eu.store.ui.com/products/dream-router) |
| [Philips Hue Bridge](https://www.philips-hue.com/pt-pt/p/hue-hue-bridge/8719514342620) |
| [Philips Hue e27 800lm color - Model LCT010](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--e27/8719514328204) |
| [Philips Hue e27 1100lm color - Model LCA006](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--e27/8719514291171#specifications) |
| [Philips Hue e17 470lm color - Model LCT012](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-lampada-individual-e14/8719514356610) |
| [Philips Hue Gu10 350lm color - Model LCG002](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--gu10/8719514339880) |
| [Philips Hue GO V1 - Model LLC020](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-luz-portatil-go--modelo-mais-recente-/7602031P7) |
| [Philips Hue GO V2 - Model LCT026](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-luz-portatil-go--modelo-mais-recente-/7602031P7) |
| [Philips Hue Playbar - Model LCT024](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-embalagem-dupla-de-barra-de-luz-play/7820230P7) |
| [Philips Hue Dimmer Switch](https://www.philips-hue.com/en-us/p/hue-dimmer-switch--latest-model-/046677562779) |
| [LELLKI Zigbee Power Strip](https://s.click.aliexpress.com/e/_DmGSd6r) |  
| [LELLKI Zigbee Plug Wall Socket EU](https://s.click.aliexpress.com/e/_Dlp2U4R) | 
| [LELLKI Zigbee Smart Life Plug 16A EU Zigbee](https://s.click.aliexpress.com/e/_DdiBH2n) |   
| [LELLKI ZigBee Light Switch Smart Wall On Off](https://s.click.aliexpress.com/e/_DBme06F) | 
| [LELLKI Zigbee Switch Controller](https://s.click.aliexpress.com/e/_DkA6EBN) | 
| [LELLKI Zigbee Power Strip Energy Monitoring](https://s.click.aliexpress.com/e/_DdlEJAX) | 
| [LELLKI Zigbee Smart Wall Socket 220v Energy Monitoring](https://s.click.aliexpress.com/e/_DmrUn4T) | 
| [LELLKI Zigbee Tuya 220V Smart Switch 25A Plug Energy Monitoring](https://s.click.aliexpress.com/e/_DeKDxEr) | 
| [LELLKI Zigbee Light Switch Energy Monitoring](https://s.click.aliexpress.com/e/_Deu1uTH) | 
| [LELLKI ZigBee Light Switch EU Glass Smart Touch](https://s.click.aliexpress.com/e/_Ddlvb5z) |
| [LELLKI Zigbee Gateway Tuya Hub Smart Life Wireless Bridge](https://s.click.aliexpress.com/e/_DCIq0hv) |   
| [Zigbee Door And Window Magnetic Sensor ](https://s.click.aliexpress.com/e/_DmJH6ix) |     
| [Zigbee Human Motion Sensor Smart Home PIR Motion](https://s.click.aliexpress.com/e/_DeZ8QZh) | 
| [ZigBee Temperature And Humidity Sensor](https://s.click.aliexpress.com/e/_DBl75hz) | 
| [Moes ZigBee Brightness Thermometer Humidity Sensor](https://s.click.aliexpress.com/e/_DllGUur) | 
| [Moes ZigBee Smart Home Temperature And Humidity Sensor](https://s.click.aliexpress.com/e/_DkTzler) | 
| [Moes WiFi Tuya Smart IR Remote ](https://s.click.aliexpress.com/e/_DCboWiT) | 
| [Moes Zigbee Mini DIY Dimmer Switch Module](https://s.click.aliexpress.com/e/_Dkrbhpl) |   
| [Benexmart Zigbee Tuya LED Dimmable Downlight](https://s.click.aliexpress.com/e/_DdjASgR) | 
| [Benexmart Zigbee 3.0 Smart LED Downlight for Ceiling ](https://s.click.aliexpress.com/e/_DdP3shp) | 
| [Benexmart Zigbee Power Socket  16A ](https://s.click.aliexpress.com/e/_DBvcvFZ) | 
| [Zemismart WiFi Switch Module Mini Switch](https://s.click.aliexpress.com/e/_DCusjFh) |  
| [Zemismart Zigbee 3.0 Wireless Switch 4 Gang Smart Scene Switches](https://s.click.aliexpress.com/e/_DBj46ij) | 
| [Zemismart Zigbee Temperature and Humidity Sensor](https://s.click.aliexpress.com/e/_Dkh8yZv) | 
| [Zemismart Zigbee PIR Infrared PIR Motion Detection Smart Sensor](https://s.click.aliexpress.com/e/_DeWxs8r) | 
| [Zemismart 6 channels Tuya Zigbee Wireless Switch](https://s.click.aliexpress.com/e/_DesRa79) |  
| [AUESS 16/10A Tuya MINI WiFi Switch 2-way](https://s.click.aliexpress.com/e/_DdSKtOf) |  
| [SONOFF NSPanel Smart Touch Scene Wall Switch EU](https://s.click.aliexpress.com/e/_DDOkMnH) |  
| [SONOFF MINI R2 DIY Smart Wifi Switch 2 Way]() |  
| [SONOFF Mini R3 16A Wifi Bluetooth Smart Switch](https://s.click.aliexpress.com/e/_Ddh3P1H) |  
| [SONOFF Basic R2 Wifi DIY Smart Switch ](https://s.click.aliexpress.com/e/_DFtgFYx) |  
| [Sonoff 4CH R3 PROR3 Smart DIY Switch 4 Channel Din Rail ](https://s.click.aliexpress.com/e/_DDcNQJV) |  
| [SONOFF ZBBridge Smart Zigbee Bridge Zigbee 3.0 ](https://s.click.aliexpress.com/e/_DDwW9Lt) |  
| [SONOFF ZBMINI-L Zigbee Smart Switch No Neutral](https://www.aliexpress.com/item/1005001392385579.html) |  
| [SONOFF WiFi Smart LED Bulb B05-BL B02-BL E26/E27](https://s.click.aliexpress.com/e/_Dd1RYXN) |  
| [SONOFF L2 LED Light Strip L1-lite 5M 5050 RGB](https://s.click.aliexpress.com/e/_DDBhFRp) |  
| [SONOFF TH-16 Smart Wifi Switch 16A/3000W Monitoring Temperature Sensor RF433](https://s.click.aliexpress.com/e/_Des1nZV) |
| [SP511E 24V 38key RGB Controller ](https://s.click.aliexpress.com/e/_DcfyTkT) |  
| [Sp501E Wifi Led Controller](https://s.click.aliexpress.com/e/_Dn2uU9h) |  
| [Led Strip WS2811 12v 60leds/M](https://s.click.aliexpress.com/e/_DeoNw4f) |  
| [Neon Led Strip WS2811 12v 60leds/M](https://s.click.aliexpress.com/e/_DdqMD8x) |  
| [Smart ZigBee Energy Meter Single Phase 80A Din Rail Power Monitor](https://s.click.aliexpress.com/e/_DDHlbgj) |  
| [Tuya Smart Zigbee 220V Switch 4 Channel With Ding Rail Housing](https://s.click.aliexpress.com/e/_DkyxuIF) |  
| [Bingoelec Energy Monitor Smart Socket Wifi Outlet](https://s.click.aliexpress.com/e/_Dm7pZ9H) |
| [Yagusmart Zigbee 3.0 Smart Inline Dimmer Switch](https://s.click.aliexpress.com/e/_DlCyuKx) |
| [Yagusmart Tuya WiFi Switch Smart Push Button 1 2 3 Gang Neutral Wire](https://s.click.aliexpress.com/e/_DljJeht) |
| [Yagusmart Zigbee Smart Switch Tuya Wireless Push Button](https://s.click.aliexpress.com/e/_DkMNIw7) |
| [Yagusmart Tuya ZigBee Smart Light Switch with Touch Panel No Neutra](https://s.click.aliexpress.com/e/_DlFpTsb) |
| [Tuya ZigBee Smart Battery Switch Wire Free 1/2/3 Gangs Touch Switch Sticke](https://www.aliexpress.com/item/4001217084809.html) |
| [eWeLink Single Live Wire WIFI Module DIY mini wifi switch Timer Light Switch Remote Control Module](https://www.aliexpress.com/item/4000727182744.html) |  
| [OWYEAN Smart ZigBee 3.0 16A Mini DIY Switch Relay Breaker ](https://s.click.aliexpress.com/e/_DmPGTBt) |  
| [Paul Neuhaus Q-Mia RGBW LED spotlight/wall light with dimmer and CCT -  9185-13](https://www.reuter.com/paul-neuhaus-q-remote-for-q-light-fittings-w-38-h-151-d-15-cm-black-a737280.php) | 
| [Paul Neuhaus Q-Erik RGBW LED ceiling ligh](https://www.paul-neuhaus.de/fileadmin/user_upload/paul-neuhaus/Landingpage/Q-Booklet_englisch_WEB_2017.pdf) | 
| [Nvidea Shield 2017](https://www.cnet.com/reviews/nvidia-shield-tv-2017-review/) |  
| [Google Nest Hub](https://store.google.com/us/product/nest_hub_2nd_gen?pli=1&hl=en-US) | 
| [Google Mini V2](https://www.tek4life.pt/pt/coluna-inteligente-google-nest-mini-2-geracao-preto) | 
| [Lenovo Smartclock Essencials](https://www.lenovo.com/us/en/p/smart-devices/smart-home/smart-home-series/smart-clock-essential) | 
| [Lenovo SmartDisplay 7"](https://www.lenovo.com/gb/en/smart-display/) | 
| []() | 
  
</details>
### Custom Components Used

 ---
## Screenshots

## HA Supervisor

### Addon Repositories

### Addons

## Licence

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or distribute this software, either in source code form or as a compiled binary, for any purpose, commercial or non-commercial, and by any means.

In jurisdictions that recognize copyright laws, the author or authors of this software dedicate any and all copyright interest in the software to the public domain. We make this dedication for the benefit of the public at large and to the detriment of our heirs and successors. We intend this dedication to be an overt act of relinquishment in perpetuity of all present and future rights to this software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to [https://unlicense.org](https://unlicense.org)

<p align="right"><a href="#top" title="Back to top">Top</a></p>

## Other Good HA Resources/Configs



![image](https://user-images.githubusercontent.com/32928749/189365835-60fbf4ef-b4fd-40a2-87df-c42eca44ccd6.png)

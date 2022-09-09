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
  - I run three VMs from this machine, one for Home Assistant (Using HassOS) and the other two for other home server stuff

### Zigbee

I'm running a combination of Chinese sensors for doors, Aqara for movement, switchs and modules from several chinese brands and a ZZH as the host in Zigbee2Mqtt
I also use alot of Phlips hue Bulds coneected to a few Hue Bridges
<p align="right"><a href="#top" title="Back to top">Top</a></p>

---

## Stats

_Stats as at 05:00, Thursday, June 23rd 2022_

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
</details>

<details>
<summary>Devices list</summary>
| Name |
| --- |
| [zone](https://www.home-assistant.io/components/zone) |
| [Philips Hue Bridge](https://www.philips-hue.com/pt-pt/p/hue-hue-bridge/8719514342620) |
| [Philips Hue e27 800lm color - Model LCT010](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--e27/8719514328204) |
| [Philips Hue e27 1100lm color - Model LCA006](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--e27/8719514291171#specifications) |
| [Philips Hue e17 470lm color - Model LCT012](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-lampada-individual-e14/8719514356610) |
| [Philips Hue Gu10 350lm color - Model LCG002](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-pacote-de-1--gu10/8719514339880) |
| [Philips Hue GO V1 - Model LLC020](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-luz-portatil-go--modelo-mais-recente-/7602031P7) |
| [Philips Hue GO V1 - Model LCT026](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-luz-portatil-go--modelo-mais-recente-/7602031P7) |
| [Philips Hue Playbar - Model LCT024](https://www.philips-hue.com/pt-pt/p/hue-white-and-color-ambiance-embalagem-dupla-de-barra-de-luz-play/7820230P7) |
| [Philips Hue Dimmer Switch](https://www.philips-hue.com/en-us/p/hue-dimmer-switch--latest-model-/046677562779) |
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

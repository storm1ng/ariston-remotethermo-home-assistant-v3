[![CodeQL](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/codeql.yml/badge.svg?branch=main)](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/codeql.yml)
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://hacs.xyz)
[![HACS Action](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/hacs.yml/badge.svg)](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/hacs.yml)
[![Validate with hassfest](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/hassfest.yml/badge.svg)](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3/actions/workflows/hassfest.yml)
# Ariston NET remotethermo integration for Home Assistant

> **Note on the official Ariston integration & rebranding**
> Home Assistant now ships an official `ariston` integration, but it only supports midea-protocol climate devices (cooling). To avoid a domain collision with it, this integration uses the domain `ariston_remotethermo` instead of `ariston`, so both can be installed side by side. It continues to support Galevo/Velis/BSB heating and water-heater devices via the reverse-engineered RemoteThermo API.
>
> This is a fork of [fustom/ariston-remotethermo-home-assistant-v3](https://github.com/fustom/ariston-remotethermo-home-assistant-v3) — full credit to [fustom](https://github.com/fustom) and [Chomupashchuk's v2 integration](https://github.com/chomupashchuk/ariston-remotethermo-home-assistant-v2) for the original work.
>
> **Migration:** because the domain changed, existing users must remove the old `ariston` custom integration and re-add this one. Devices, entities and history are recreated under the new domain (clean break, no automatic migration).

This integration inspired by chomupashchuk fantastic work https://github.com/chomupashchuk/ariston-remotethermo-home-assistant-v2
But it does not use Ariston website. It uses Ariston API what I reversed engineered.


| [This integration](https://github.com/storm1ng/ariston-remotethermo-home-assistant-v3)
| ------------- | ------------- |
| Uses real API  | Uses Ariston website  |
| Faster set/get data  | Sometimes needs minutes to set/get data |
| Easy to setup with UI | Not so easy to setup (only with configuration.yaml) |
| Integration & devices & entites | Only entites |
| Proper asynchronous integration, clean code | Hard to understand and maintain (ariston.py has more than 4000 lines) |
| Less sensors, switches, etc |  More sensors, switches, etc |
| New code, may contains lot of bugs | Old, tested code |

## TODO
- Localization. Avaliable in english, catalan, italian, russian and ukranian.
- More sensors, switches, binary sersors, selectors, services.
- Exception handling.
- More logs.
- Unit tests.
- Fun.

## Integration was tested on and works with:
- Ariston Alteas One 24
- Ariston Velis Evo
- Ariston Velis Lux
- Ariston Lydos Hybrid
- Elco Thision S Plus 13

Feel free to test something else and create new issue / pull request if something goes wrong.

## Installation
[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=storm1ng&repository=ariston-remotethermo-home-assistant-v3&category=integration) or copy the ariston_remotethermo folder to your configuration/custom_components path.
Use the add integration UI to set up your device.

| ![Kazam_screenshot_00003](https://user-images.githubusercontent.com/6751243/146653448-ff7b6f9d-cbf1-4555-9a75-61bf68bc9d3e.png) | ![Kazam_screenshot_00004](https://user-images.githubusercontent.com/6751243/146653484-52e39d78-7c6f-44ae-888d-acf246147290.png) | ![Kazam_screenshot_00010](https://user-images.githubusercontent.com/6751243/147890590-6c4ebf38-16d9-421f-9b81-8f43298ec62f.png) |
:-------------------------:|:-------------------------:|:-------------------------:

![Kazam_screenshot_00011](https://user-images.githubusercontent.com/6751243/147890611-54ae2d28-bf5a-45f8-ba92-e7a00a22615c.png)

![Kazam_screenshot_00012](https://user-images.githubusercontent.com/6751243/147989103-cdac510f-e6f6-461f-a88e-b8ff0204c34f.png)

| ![Kazam_screenshot_00013](https://user-images.githubusercontent.com/6751243/148247717-5211c01c-561f-4a4e-b4b5-47a680e04a68.png) | ![Kazam_screenshot_00009](https://user-images.githubusercontent.com/6751243/146657797-ed14b741-595a-48a6-9126-1acca3beb69f.png) |
:-------------------------:|:-------------------------:

<h1 align="center">Peace Love Freedom</h1>

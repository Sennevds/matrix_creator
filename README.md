# matrix_creator
Custom component for Home Assistant using the Matrix Creator

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE.md)
<!-- [![GitHub Activity][commits-shield]][commits] -->

<!-- ![Project Maintenance][maintenance-shield1] -->
<!-- ![Project Maintenance][maintenance-shield2] -->
This project is based on the official [Sense HAT](https://www.home-assistant.io/components/sensehat) component for Home Assistant
Use the [Matrix Creator](https://www.matrix.one/products/creator) sensors in Home Assistant
Currently only following sensors are supported:
    - Humidity
    - Temperature
    - Pressure
    - UV

To get started put `/custom_components/matrix_creator/` here:
`<config directory>/custom_components/matrix_creator/`

**Example configuration.yaml:**
```yaml
sensor:
  - platform: matrixcreator
    display_options:
      - temperature
      - humidity
      - pressure
      - uv
```
**Configuration variables:**

Field | Value | Necessity | description
:--- | :---
**platform** | matrixcreator | Required
**display_options** | temperature, humidity, pressure, uv | Required | The sensors you want to add
**is_hat_attached** | true | Optional | Is the HAT directly connected to the RPI


***
Due to how `custom_components` are loaded, it is normal to see a `ModuleNotFoundError` error on first boot after adding this, to resolve it, restart Home-Assistant.

<!-- ## Like this component for home-assistant?

| Donate | Developers |
| --- | --- |
| <a href="https://www.paypal.me/swetoast"><img align="center" src="https://gitlab.com/swe_toast/asustor_firewall/raw/master/images/Untitled.png"></a>   | <a href="https://github.com/swetoast">Toast</a></div> |
| <a href="https://www.buymeacoffee.com/zJtVxUAgH"><img align="center" src="https://www.buymeacoffee.com/assets/img/custom_images/black_img.png"></a> | <a href="https://github.com/iantrich">Ian Richardson</a> | -->

[license-shield]: https://img.shields.io/github/license/sennevds/matrix_creator.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/sennevds/matrix_creator.svg?style=for-the-badge
[releases]: https://github.com/sennevds/matrix_creator/releases
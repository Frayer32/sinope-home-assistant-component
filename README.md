# Home Assistant Sinopé Custom Components

Custom components for Sinopé thermostats in Home Assistant. (http://www.home-assistant.io)

## Installation
Copy the sinope.py component to your custom component climate directory.
Example: 
```
# Create required dirs
mkdir ~/.homeassistant/custom_components
mkdir ~/.homeassistant/custom_components/climate
cd /home/homeassistant/.homeassistant/custom_components/climate/
wget https://raw.githubusercontent.com/ryanmaclean/sinope-home-assistant-component/master/custom_components/climate/sinope.py
```

## Configuration

To enable your Sinopé thermostats management in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
climate:
  - platform: sinope
    username: '<your e-mail-adress>'
    password: '<your Neviweb password>'
    gateway: '<your gateway name>'
```

Configuration variables:

- **username** (*Required*): The email address that you use for Sinopé Neviweb.
- **password** (*Required*): The password that you use for Sinopé Neviweb.
- **gateway** (*Required*): The name of the network you wan't to control.

N.B. these values can be retrieved form the [Neviweb portal](https://neviweb.com/)

## Restart Home Assistant

`sudo systemctl restart home-assistant`

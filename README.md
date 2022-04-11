# broadlink-custom-component

Custom component based on the [official Broadlink component](https://github.com/home-assistant/core/tree/dev/homeassistant/components/broadlink) for Home Assistant. This custom component will override the Broadlink component.

This component is a temporary workaround to be able to add devices that operate under a mesh network due to the [Broadlink FastCon technology](https://www.broadlink.ae/post/what-is-broadlink-fastcon-technology).

## Install

1. Launch the [Terminal and SSH](https://github.com/home-assistant/addons/tree/master/ssh) add-on in Home Assistant
2. Run the following:

```bash
$ mkdir -p ~/config/custom_components
$ cd ~/config
$ wget -O - https://github.com/bendamschke/broadlink-custom-component/archive/main.tar.gz | tar xz --strip=1 "broadlink-custom-component-main/custom_components/broadlink"
```

3. Restart Home Assistant
4. Launch the [Terminal and SSH](https://github.com/home-assistant/addons/tree/master/ssh) add-on in Home Assistant
5. Run the following:

```bash
$ echo "broadlink:" >> ~/config/configuration.yaml
```

6. Check Home Assistant configuration in the settings to ensure it passes.
7. Restart Home Assistant
8. Add in Broadlink components via their host, MAC and [device type](https://github.com/mjg59/python-broadlink/blob/master/broadlink/__init__.py#L18=).

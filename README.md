# Raspberry Pi - Kubernetes - Cluster

### Hardware
 - 1 x Raspberry Pi 4 4GB (Host)
 - 3 x Raspberry Pi 3b+ (Workers)
 - 3 x micro usb to usb A
 - 1 x usc C to usb A
 - 1 x usb PSU
 - 1 x minimum 4 port switch
 - 4 x 32GB USB-storage

### Setting up for usb boot

 1. Install Ubuntu server (64-bit) to all the USB-storages using https://www.raspberrypi.org/software/
 2. `cd` to `system-boot` in volumes and edit `network-config` file to add your wifi name and pass
```yml
wifis:
  wlan0:
  dhcp4: true
  optional: true
  access-points:
    "home network":
      password: "123456789"
```

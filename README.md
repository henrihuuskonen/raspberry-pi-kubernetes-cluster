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

1. Update EEPROMs on all Pis
2. Set boot order to USB first, if that fails then SD card

### Loading OS to USB-storages

1. Download 64-bit Raspberry Pi OS  
- This was at the time of writing in beta
- https://www.raspberrypi.org/forums/viewtopic.php?t=275370

### Enable ssh on each

```
cd ~/Volumes/boot
touch ssh
```

### Initial setup

1. Find each Pi's IP address
2. `ssh pi@xxx.xxx.xx.xx`
3. `sudo raspi-config`
  1. Change hostname
  2. Change password
  3. Setup wifi (optional)
  4. Reboot `sudo reboot`
4. Update everything `sudo apt update && sudo apt upgrade && sudo reboot`

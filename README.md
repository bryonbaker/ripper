# Disk Image for Ansible Invaders

## Burning a disk
Instructions have only been tested on Fedora... They will work for MacOS - no idea about Windoze.

1. Download the disk image as a raw file.
2. Valuidate the SHA using openssl
    ```
    $ openssl dgst --sha256 sdcard_backup.img
    SHA2-256(sdcard_backup.img)= 43d6c2321048f0387401ff3e40e1621ad3cbb1faa467f54e6baf4e7dec060369
    ```
3. If the SHA matches the above, insert the SD Card into your laptop and identify the device. E.g. /dev/sda4
4. Copy the image to the device. E.g.:
   ```
  $ sudo dd if=./sdcard_backup.img of=<your device> bs=4M status=progress
   ```

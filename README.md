## WHAT 
Create your own base Alpine Linux container for Raspberry Pi 2 / ARM7.

## WHY
There are public images freely available, I wanted to create/control my own.

## HOW
### Build it
- Git clone this repo on your Raspberry Pi
- Run the `mkimage-alpine.sh` script
- Verify that the images were created `docker images`

### Transfer the image (optional)
- Save the image as a .tar file
  - `docker save -o docker-alpine-rpi.tar docker-alpine-rpi`
- SCP the image to another machine (run this from a remote machine with SSH access to your rpi)
  - `scp <rpi-user>@<rpi-ip>:/<rpi-filepath>/docker-alpine-rpi.tar <local-filepath>`
- Load the image
  - `docker load -i <path to image tar file>`

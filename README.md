# radxa-zero-dtb-overlays
Device tree overlays for i2C, SPI and other peripherals on the Radxa Zero board
## DISCLAIMER: NO GARANTEES GIVEN, NO NEW FUNCTIONALITY.
This repository is merely a cherry-picked set of files already existent in system images and repositories created/maintained/owned by Radxa for use with the Radxa Zero board. I do not garantee they will work on different kernel versions, on unpatched mainline kernels or even on the same kernel under a different distribution (Armbian, Manjaro, PostMarketOS).
## what are overlays?
Device Tree Overlays change what devices are enabled on the system at boot time and how they are set up. In the radxa-zero's case, the overlays that may be picked by the user toggle functions on the 40-pin header for the many peripherals, including i2C, PWM, SPI, UART and others.
## how do i use them?
copy the overlays to your installation's dtb (Device Tree Binary) overlay folder (usually at /boot/dtbs/overlays), then add them to the "overlays=..." line on the environment file for your system. **the folders provided here usually have detailed instructions for each overlay, please do read it before proceeding.**
## i have no idea what is all this, but i want the peripherals.
Here's a quick guide to enable peripherals hassle-free.
### Plan A: use official radxa debian
 Install their latest stable debian image, edit `overlays` line at /boot/uEnv.txt according to radxa's official overlays guide.
